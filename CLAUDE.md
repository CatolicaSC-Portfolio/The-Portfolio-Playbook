# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## O que este repositório é

Repositório **somente de documentação** (PT-BR). Não há código, build, testes nem dependências. É o
regulamento das três disciplinas de Portfólio da Católica SC: define o que o aluno entrega, com que
critérios é avaliado e com que nota é aprovado. O público leitor são **alunos e professores
avaliadores** — o texto é normativo, não descritivo.

## Arquitetura: uma teia de regras, não uma árvore de arquivos

Os documentos se referenciam entre si e **repetem as mesmas regras em contextos diferentes**. É essa
duplicação intencional que define o trabalho aqui: alterar um número em um arquivo sem propagar para
os outros produz contradição normativa — o aluno e o avaliador passam a ler regras diferentes sobre o
mesmo fato. O histórico do repo é em boa parte a correção desse tipo de divergência.

`calendario.md` (raiz) é a **fonte única de datas** e traz o checklist cronológico do aluno. Nunca
introduza uma data nova em outro documento sem acrescentá-la lá — há script de verificação abaixo.

Os três documentos de disciplina estão na raiz e o `README.md` indexa tudo. Dois pontos que o `ls` não
conta: `directions/portfolio-directions-GERAL.md` traz a **tabela mestra** de tecnologias, processos e
temas (🔑 Obrigatório · ✅ Preferir · 🔍 Explorar · ⚠️ Evitar · 🚫 Não Usar), e `semesters/` guarda
planilhas de notas por turma — **gitignorado, nunca versionar**.

Os binários versionados (`Contrato-Pedagogico-Portfolio-PAC-VIII.pptx`, `demoday/TEMPLATE_POSTER_PORTFOLIO.*`)
também repetem regras, mas nem `grep` nem os verificadores os enxergam. Quando uma regra mudar, avise que
eles precisam de revisão manual.

Documentos de trabalho derivados, como `Plano-de-Ensino-PAC-VIII.md` (formulário institucional), recebem
conteúdo dos normativos e nunca o contrário.

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
| **Playtest obrigatório só em Jogos**: mínimo de **10** participantes; noite oficial **26/10/2026** ou playtest independente com evidências; relatório até **30/10/2026**. Playtest com público externo segue como **diferencial** | `documentation/games/Diretrizes-Playtest.md` | `directions/portfolio-directions-jogosdigitais.md` (obrigatório · diferencial · régua) · `calendario.md` |
| Núcleo comum de engenharia — **4 itens**: Wiki · CI/CD · análise estática · monitoramento/observabilidade | `directions/portfolio-directions-GERAL.md` | replicado sob `### Núcleo comum de engenharia` nas cinco directions |

**Testes não são iguais entre as linhas** — esta é a assimetria mais fácil de quebrar por engano:

| Linha | Meta obrigatória | TDD |
|---|---|---|
| **Web Apps** | **75% backend / 25% frontend** | 🔑 obrigatório |
| **Mobile · IA · IoT · Jogos Digitais** | **nenhuma** — testes unitários não se aplicam bem a essas tecnologias | ✅ preferir |

Nessas quatro linhas os testes vivem em *O que é desejável atender*, com o instrumento próprio de cada uma
(instrumentados/integração · validação de modelo · rotinas críticas de firmware · lógica de jogo). Jogos
teve meta de 50% até 21/10/2026 (item E1 do relatório). Mobile volta a ter TDD
obrigatório **se o aluno escrever o próprio backend**. A meta é **gate conferido na prova de autoria**, não
item de nota — o critério 3 do Demo Day pontua a *qualidade* dos testes, e penaliza teste raso que só
persegue percentual. Cobertura **não** está no núcleo comum, justamente por não ser comum.

As cinco directions têm **as mesmas 9 seções nos mesmos níveis** (`## O que é obrigatório atender` com
`### Núcleo comum de engenharia` dentro · desejável · diferencial · deve ser evitado · não pode ter ·
temas a evitar · temas impedidos · `## Régua de Avaliação`). Há script de verificação abaixo.

**Exceções da linha de Jogos Digitais** — recorrem em vários documentos e são a origem mais comum de
contradição: repositório pode ser privado (com acesso aos avaliadores) e o "ambiente produtivo em
nuvem" é satisfeito por build pública distribuída (Itch.io, loja, WebGL, APK).

## Convenções de escrita

- **Datas:** sempre `DD/MM/AAAA` **seguido do dia da semana** — `30/11/2026 (segunda-feira)`. Em
  tabelas, o dia da semana pode ocupar coluna própria. Data por extenso ("16 de outubro de 2026") quebra
  a convenção **e escapa do verificador de datas órfãs**, que só reconhece `DD/MM/AAAA`.
- **Links:** os documentos usam URL absoluta
  `https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/<caminho>`, com `%20` nos
  espaços. Só o `README.md` usa caminhos relativos. Migrar tudo para relativo é item aberto (B1 no
  relatório) — até que seja decidido, **siga o estilo do arquivo que está editando**.
- **Projeto é individual.** Nunca escrever "equipe" ou "grupo" (foi corrigido em M3).
- **Directions específicas** seguem o esqueleto fixo, hoje idêntico nas cinco — ver a tabela de testes
  acima. Ao criar ou editar uma direction, mantenha o esqueleto e a ordem, e rode o script de simetria.
- **Sanção tem um nome só: "reprovação".** Não use "desclassificação" — o termo foi eliminado do
  repositório porque criava uma terceira categoria sem consequência definida.
- **GDD:** `documentation/games/GDD - Template.md` e `GuiaPreenchimenteBoasPraticas.md` têm as
  **mesmas 19 seções numeradas, na mesma ordem**. Mexer em uma exige mexer na outra.
- **Emoji nos títulos** é usado em alguns documentos (`## 🔑 Formato de Avaliação`). Preserve o
  padrão do arquivo; não introduza nem remova por conta própria.

## Verificação (o "test suite" deste repo)

Este repositório não tem build nem testes; o equivalente são quatro verificadores de consistência —
links internos, seções da RFC citadas nas diretrizes, datas órfãs fora do `calendario.md` e simetria
estrutural das cinco directions, mais o alinhamento GDD Template × Guia.

**Rode-os pela skill `verificar-consistencia`** (`.claude/skills/verificar-consistencia/SKILL.md`)
sempre que editar links, numeração de seções, prazos, o GDD ou qualquer arquivo em `directions/`, e antes
de considerar uma rodada de correções concluída.

## Catalogue a inconsistência antes de corrigir

Ao encontrar uma contradição entre documentos, **registre o problema — arquivos e linhas dos dois lados
— antes de editar**, e depois escreva por que a resolução é essa. O valor está em explicar *por que* a
regra é o que é hoje; sem isso a próxima pessoa redescobre a mesma divergência e pode desfazer a decisão.

Há um livro-razão dessa auditoria em `RELATORIO-INCONSISTENCIAS.md`, com 71 itens fechados em três
rodadas. Ele é **documento de trabalho local e não versionado** (está no `.gitignore`), então pode não
existir num clone novo — se não estiver presente, comece um. Duas recomendações registradas lá seguem
**não executadas**, ambas sem impacto normativo: padronizar todos os links em caminhos relativos, e
resolver a colisão de numeração dentro da Seção 5.1 da RFC.

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
