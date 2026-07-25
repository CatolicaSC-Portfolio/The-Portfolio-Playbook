# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## O que este repositório é

Repositório **somente de documentação** (PT-BR). Não há código, build, testes nem dependências. É o
regulamento das três disciplinas de Portfólio da Católica SC: define o que o aluno entrega, com que
critérios é avaliado e com que nota é aprovado. O público leitor são **alunos e professores
avaliadores** — o texto é normativo, não descritivo.

Repo remoto: `github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook` · branch de produção: `main`.

## Arquitetura: uma teia de regras, não uma árvore de arquivos

Os documentos se referenciam entre si e **repetem as mesmas regras em contextos diferentes**. É essa
duplicação intencional que define o trabalho aqui: alterar um número em um arquivo sem propagar para
os outros produz contradição normativa — o aluno e o avaliador passam a ler regras diferentes sobre o
mesmo fato. O histórico do repo é em boa parte a correção desse tipo de divergência (ver
`RELATORIO-INCONSISTENCIAS.md`).

**Três eixos de disciplina** (raiz):

| Arquivo | Semestre | Entrega central |
|---|---|---|
| `PAC Extensionista VII.md` | 7º | RFC aprovada, aplicada a problema real de parceiro externo ou comunidade |
| `PAC Extensionista VIII.md` | 8º | Validação extensionista + peer review (NP1 20% / NP2 20% / NP3 60%) |
| `Portfolio.md` | 8º | Produto em produção, prova de autoria, Poster + Demo Day |

`README.md` é o índice de navegação de tudo.

**Quatro diretórios de apoio:**

- `directions/` — cinco linhas de projeto (webapp, mobile, jogosdigitais, ia, iot) +
  `portfolio-directions-GERAL.md`, que traz a tabela mestra de tecnologias/processos/temas com quatro
  veredictos: 🔑 Obrigatório · ✅ Preferir · 🔍 Explorar · ⚠️ Evitar · 🚫 Não Usar.
- `demoday/` — critérios de avaliação, guia do pôster, provedores de hospedagem, templates `.pptx`/`.pdf`.
- `documentation/` — `RFC/modelo-de-RFC.md` (627 linhas, artefato do 7º sem.),
  `diretrizes-avaliacao-professores.md` (como avaliar a RFC), `normas.md` (LGPD/licenças/setoriais),
  `games/` (GDD Template + Guia de Preenchimento).
- `semesters/` — planilhas de notas por turma. **Gitignorado**, nunca versionar.

## Fonte única de verdade por regra

Antes de escrever qualquer número, confira aqui de onde ele vem. Se a mudança for numa dessas regras,
propague para **todos** os arquivos abaixo que a mencionam.

| Regra | Fonte canônica | Também aparece em |
|---|---|---|
| Nota do Demo Day: Likert 1–5 → 0–10 (**×2**); professores **90%** / comunidade **10%**; 1 casa decimal | `demoday/Avaliacao_Poster_DemoDay.md` § *Como a Likert vira nota* | `Portfolio.md` § Avaliação |
| 6 critérios de peso igual; **critério 5 (Ética/Autoria) é eliminatório**; piso da fórmula 2,0 | `demoday/Avaliacao_Poster_DemoDay.md` | `Portfolio.md` § Prova de Autoria |
| Nota da RFC: 0–10 em passos de **0,5**; aprovação a partir de **6,0**; faixa **6,0–7,0 = aprovada com correções obrigatórias** | `documentation/diretrizes-avaliacao-professores.md` § Anexo - Escala | `documentation/RFC/modelo-de-RFC.md` § 10 (ficha por avaliador + Consolidação) |
| Prazo de entrega **30/11/2026 (segunda-feira)**; Demo Day **10/12**, **15/12**, **16/12/2026** | `Portfolio.md` § Datas e Prazos | `PAC Extensionista VIII.md` § Prazos |
| **Seis participações obrigatórias**: 5 orientações (2 até **30/09/2026**, todas até 30/11) = gate de **habilitação**; 1 noite como visitante + avaliar os colegas = gate de **aprovação** | `Portfolio.md` § Requisitos de Aprovação | `Portfolio.md` § Requisitos de Entrega · `demoday/Avaliacao_Poster_DemoDay.md` § Pré-condição e § Participação da Comunidade · `demoday/guia_poster.md` § Participação |
| **Prova de autoria**: verifica autoria **e a cobertura de testes da linha**; admite **uma segunda tentativa** até **03/12/2026**; reprovar duas vezes = reprovado na disciplina, sem apresentar | `Portfolio.md` § Prova de Autoria | `demoday/Avaliacao_Poster_DemoDay.md` § Pré-condição e critério 3 · `demoday/guia_poster.md` |
| **Calendário do PAC VII é próprio** (7º período) e não compartilha datas com Portfólio/PAC VIII (8º período) | `PAC Extensionista VII.md` § 6. Prazos | — |
| Régua Destaque / Aprovado / Reprovado; aprovado exige nota ≥ **6,0** | cada `directions/portfolio-directions-*.md` § Régua de Avaliação | — |
| Núcleo comum de engenharia (5 itens: Wiki · CI/CD · análise estática · observabilidade · cobertura de testes) | `directions/portfolio-directions-GERAL.md` | replicado literalmente em cada direction específica |

**Cobertura de testes é por linha, não global:** webapp e mobile 75% backend / 25% frontend · ia 70% ·
iot 60% · jogosdigitais 50%. Cada direction também declara o que fica **fora** da contagem (notebooks,
engine, shaders, assets, firmware não crítico). A cobertura é **gate conferido na prova de autoria**, não
item de nota — o critério 3 do Demo Day pontua a *qualidade* dos testes. Os números vivem em **três**
lugares (direction · `Portfolio.md` § Prova de Autoria · critério 3): mudar um exige mudar os três.

**Exceções da linha de Jogos Digitais** — recorrem em vários documentos e são a origem mais comum de
contradição: repositório pode ser privado (com acesso aos avaliadores) e o "ambiente produtivo em
nuvem" é satisfeito por build pública distribuída (Itch.io, loja, WebGL, APK).

## Convenções de escrita

- **Datas:** sempre `DD/MM/AAAA` **seguido do dia da semana** — `30/11/2026 (segunda-feira)`. Em
  tabelas, o dia da semana pode ocupar coluna própria.
- **Links:** os documentos usam URL absoluta
  `https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/<caminho>`, com `%20` nos
  espaços. Só o `README.md` usa caminhos relativos. Migrar tudo para relativo é item aberto (B1 no
  relatório) — até que seja decidido, **siga o estilo do arquivo que está editando**.
- **Projeto é individual.** Nunca escrever "equipe" ou "grupo" (foi corrigido em M3).
- **Directions específicas** seguem o esqueleto fixo: `O que é obrigatório atender` (+ `### Núcleo
  comum de engenharia`) · `O que é desejável atender` · `O que é um diferencial` · `O que deve ser
  evitado` · `O que não pode ter` · [`Temas a evitar` · `Temas impedidos`] · `Régua de Avaliação`.
  Ao criar ou editar uma direction, mantenha o esqueleto e a ordem.
- **GDD:** `documentation/games/GDD - Template.md` e `GuiaPreenchimenteBoasPraticas.md` têm as
  **mesmas 19 seções numeradas, na mesma ordem**. Mexer em uma exige mexer na outra.
- **Emoji nos títulos** é usado em alguns documentos (`## 🔑 Formato de Avaliação`). Preserve o
  padrão do arquivo; não introduza nem remova por conta própria.

## Verificação (o "test suite" deste repo)

Rode estes checks depois de editar links, numeração de seções ou o GDD.

**Todos os links internos resolvem no sistema de arquivos** (absolutos + relativos, com `%20` decodificado):

```bash
python3 - <<'PY'
import re, urllib.parse, pathlib
root = pathlib.Path('.')
files = [p for p in root.rglob('*.md') if not {'.git','.remember'} & set(p.parts)]
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

**Seções da RFC citadas nas diretrizes de avaliação existem de fato** (esta divergência já quebrou o
processo de avaliação uma vez — C1 no relatório, causada por renumerar a RFC sem atualizar as diretrizes):

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

**GDD Template × Guia continuam com as 19 seções alinhadas:**

```bash
diff <(grep -oE '^#{1,2} [0-9]+\..*' 'documentation/games/GDD - Template.md' | sed -E 's/^#+ //') \
     <(grep -oE '^#{1,2} [0-9]+\..*' documentation/games/GuiaPreenchimenteBoasPraticas.md | sed -E 's/^#+ //') \
  && echo ALIGNED
```

Cuidado ao mexer na numeração da RFC: dentro de `## 5.1 Diagrama C4` existem `## 1. Nível 1`,
`## 2. Nível 2` e `## 3. Nível 3` — sub-níveis do C4 que colidem com a numeração de topo. É uma
irregularidade conhecida do template; qualquer script de numeração precisa tratá-la.

## `RELATORIO-INCONSISTENCIAS.md` — o livro-razão da auditoria

Rastreia 47 inconsistências entre os documentos (8 críticas, 17 altas, 14 médias, 8 baixas), **todas
resolvidas**. Cada item traz o problema original, os arquivos e linhas envolvidos e um bloco
`> **Resolução:**`. **Ao corrigir uma inconsistência que esteja catalogada, marque o item como
resolvido com a data e escreva o bloco de resolução** — o valor do arquivo está em explicar *por que*
a regra é o que é hoje. O mesmo vale para inconsistências novas: catalogue antes de corrigir.

Uma recomendação segue registrada e **não executada**: padronizar todos os links em caminhos relativos
(B1). Sem impacto normativo — decisão pendente.

## Decisões pedagógicas não são suas

Quando uma inconsistência só pode ser fechada escolhendo entre duas regras válidas (um peso, um
limiar, se algo é obrigatório ou desejável), **pergunte**. Não escolha por padrão nem por
plausibilidade — cada escolha vira regra que aluno e professor têm de cumprir. Correções mecânicas
(links, numeração, typos, propagação de uma regra já decidida) podem ser feitas direto.

## Git

Padrão da máquina (ver `/Users/diogo/CLAUDE.md`): branch a partir de `main`, merge **local** ao
concluir, **sem push e sem PR** salvo pedido explícito.

`.github/instructions/codacy.instructions.md` existe mas está **gitignorado** (regra de editor com IA,
não deste fluxo). Se as ferramentas MCP da Codacy estiverem disponíveis, use
`provider: gh`, `organization: CatolicaSC-Portfolio`, `repository: The-Portfolio-Playbook`.
