---
name: verificar-consistencia
description: Roda os quatro verificadores de consistência deste repositório de documentação — links internos, seções da RFC citadas nas diretrizes, datas órfãs fora do calendário e simetria estrutural das cinco directions. Use SEMPRE após editar links, numeração de seções, prazos/datas, o GDD ou qualquer arquivo em directions/, e antes de considerar uma rodada de correções concluída.
---

# Verificadores de consistência

Este repositório não tem build nem testes; estes quatro scripts são o "test suite". Rode todos e reporte
o resultado de cada um. Execute a partir da raiz do repositório.

## 1. Todos os links internos resolvem

Cobre links absolutos (`https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/...`) e
relativos, com `%20` decodificado.

```bash
python3 - <<'PY'
import re, urllib.parse, pathlib
root = pathlib.Path('.')
files = [p for p in root.rglob('*.md') if not {'.git', '.remember'} & set(p.parts)]
bad = 0
for f in files:
    for m in re.finditer(r'\]\(([^)\s]+)\)', f.read_text(encoding='utf-8')):
        u = m.group(1)
        if u.startswith('https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/'):
            tgt = root / urllib.parse.unquote(u.split('/blob/main/', 1)[1].split('#')[0])
        elif not u.startswith(('http', 'mailto:', '#')):
            tgt = f.parent / urllib.parse.unquote(u.split('#')[0])
        else:
            continue
        if not tgt.exists():
            print(f'BROKEN {f}: {u}'); bad += 1
print(f'--- {len(files)} arquivos, {bad} links quebrados')
PY
```

## 2. Seções da RFC citadas nas diretrizes existem de fato

Esta divergência já quebrou o processo de avaliação uma vez (item C1 do relatório), causada por
renumerar a RFC sem atualizar as diretrizes.

```bash
python3 - <<'PY'
import re, pathlib
rfc = pathlib.Path('documentation/RFC/modelo-de-RFC.md').read_text(encoding='utf-8')
have = set(re.findall(r'^#{1,3}\s+((?:\d+\.)*\d+)[\.\s]', rfc, re.M))
d = pathlib.Path('documentation/diretrizes-avaliacao-professores.md').read_text(encoding='utf-8')
cited = set(re.findall(r'Se(?:ção|ções)\s+\*{0,2}((?:\d+\.)*\d+)', d)) | set(re.findall(r'\*\*((?:\d+\.)\d+)\*\*', d))
print('INEXISTENTES:', sorted(cited - have) or 'nenhuma')
PY
```

Cuidado ao mexer na numeração: dentro de `## 5.1 Diagrama C4` existem `## 1. Nível 1`, `## 2. Nível 2` e
`## 3. Nível 3` — sub-níveis do C4 que colidem com a numeração de topo. Irregularidade conhecida do
template; qualquer script de numeração precisa tratá-la.

## 3. Nenhuma data existe fora do calendário

`calendario.md` é a fonte única. Qualquer data em outro documento tem de constar nele.

```bash
python3 - <<'PY'
import re, pathlib
cal = set(re.findall(r'\d{2}/\d{2}/\d{4}', pathlib.Path('calendario.md').read_text(encoding='utf-8')))
orfas = 0
for p in sorted(pathlib.Path('.').rglob('*.md')):
    if {'.git', '.remember'} & set(p.parts): continue
    if p.name in ('calendario.md', 'RELATORIO-INCONSISTENCIAS.md', 'CLAUDE.md'): continue
    for d in sorted(set(re.findall(r'\d{2}/\d{2}/\d{4}', p.read_text(encoding='utf-8')))):
        if d not in cal:
            print(f'ORFA  {p}: {d}'); orfas += 1
print(f'--- calendario tem {len(cal)} datas | {orfas} orfas')
PY
```

## 4. As cinco directions continuam estruturalmente idênticas

As cinco têm as mesmas 9 seções nos mesmos níveis (`## O que é obrigatório atender` com
`### Núcleo comum de engenharia` dentro · desejável · diferencial · deve ser evitado · não pode ter ·
temas a evitar · temas impedidos · `## Régua de Avaliação`).

```bash
python3 - <<'PY'
import re, pathlib
secs = {}
for f in sorted(pathlib.Path('directions').glob('portfolio-directions-*.md')):
    if 'GERAL' in f.name: continue
    k = f.name.replace('portfolio-directions-', '').replace('.md', '')
    secs[k] = [(len(m.group(1)), m.group(2).strip())
               for m in re.finditer(r'^(#{2,3})\s+(.+)$', f.read_text(encoding='utf-8'), re.M)]
titulos = list(dict.fromkeys(t for v in secs.values() for _, t in v))
ok = True
for t in titulos:
    row = [next((f'H{l}' for l, tt in v if tt == t), '—') for v in secs.values()]
    if len(set(row)) > 1:
        ok = False
        print(f'ASSIMÉTRICO  {t}: ' + ' '.join(f'{k}={r}' for k, r in zip(secs, row)))
print('SIMÉTRICO' if ok else '')
PY
```

## 5. GDD Template × Guia continuam com as 19 seções alinhadas

Mexer em um exige mexer no outro.

```bash
diff <(grep -oE '^#{1,2} [0-9]+\..*' 'documentation/games/GDD - Template.md' | sed -E 's/^#+ //') \
     <(grep -oE '^#{1,2} [0-9]+\..*' documentation/games/GuiaPreenchimenteBoasPraticas.md | sed -E 's/^#+ //') \
  && echo ALIGNED
```
