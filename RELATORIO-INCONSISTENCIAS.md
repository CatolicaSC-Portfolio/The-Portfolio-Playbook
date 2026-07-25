# Relatório de Inconsistências — The Portfolio Playbook

**Data da auditoria:** 25/07/2026 (sábado)
**Escopo:** 17 arquivos Markdown versionados (README, PAC VII, PAC VIII, Portfolio, disciplina-portfolio, `demoday/`, `directions/`, `documentation/`)
**Método:** leitura integral de todos os documentos + verificação HTTP dos links externos + checagem de existência dos caminhos internos.

> **Status:** este relatório é vivo. Itens marcados ✅ já foram corrigidos no repositório —
> a resolução fica registrada acima do problema original, que é preservado para histórico.

---

> **Duas rodadas.** A primeira fechou 47 itens. A **segunda rodada (25/07/2026)** releu os mesmos
> documentos com extração mecânica de números, datas, terminologia e simetria estrutural, e abriu
> **22 itens novos** — 2 críticos e 6 altos. Ver [Segunda rodada de auditoria](#-segunda-rodada-de-auditoria--25072026).

## Sumário por severidade — primeira rodada

| Severidade      | Itens        | Resolvidos      | Abertos     |
| --------------- | ------------ | --------------- | ----------- |
| 🔴 Crítico     | 8            | **8** ✅  | 0           |
| 🟠 Alto         | 17           | **17** ✅ | 0           |
| 🟡 Médio       | 14           | **14** ✅ | 0           |
| ⚪ Baixo        | 8            | **8** ✅  | 0           |
| **Total** | **47** | **47** ✅ | **0** |

> **Correção de contagem:** a primeira versão deste relatório anunciou 50 itens. A contagem real por
> seção é **47** — o excesso vinha de contar as linhas da tabela de typos (B5–B11) como itens separados.

**Nenhum item em aberto.** O último — M12, sobre o peso das orientações obrigatórias — foi fechado em
25/07/2026 com a decisão de tratá-las como gate de habilitação, ampliá-las para cinco (duas até 30/09/2026)
e acrescentar a participação como visitante no Poster + Demo Day como requisito de aprovação.

### Verificações automatizadas na última rodada

- 41 links internos checados contra o sistema de arquivos: **0 quebrados**.
- Nenhuma referência remanescente a `The-Portfolio-Playbook-I` ou `-II`.
- `GDD - Template.md`: numeração **1 a 19**, sem repetição.
- `GDD - Template.md` × `GuiaPreenchimenteBoasPraticas.md`: **19/19 seções alinhadas**.
- Links relativos do `README.md` validados.

---

## 🔴 CRÍTICO

### C1. Todas as referências de seção do RFC nas diretrizes de avaliação estão erradas — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:18-29`

> **Resolução:** a seção *Pontos a serem observados na avaliação* foi reescrita contra a numeração real
> do RFC. Cada item agora nomeia a seção correta (1.1, 1.5 · 1.2, 1.3, 1.6 · 2.1–2.4, 2.6 · 3.1, 3.2, 4.2 ·
> 5.1–5.3 · 5.4 · 6, 6.1 · 7), com uma nota de cabeçalho ligando à numeração oficial.
> Os pontos passaram de 5 para 8: foram acrescentados **Evidências e Benchmark** (1.2, 1.3, 1.6),
> **Fluxos e UX** (3 e 4) e **Planejamento** (7) — seções fortes do RFC que ninguém avaliava.

Registro do problema original:

O documento que os **professores avaliadores usam** manda olhar:

| Diretriz manda avaliar   | Seção citada | O que essa seção é hoje no RFC |
| ------------------------ | -------------- | --------------------------------- |
| Especificação técnica | 3.1            | *Fluxo Principal do Usuário*   |
| Escopo                   | 2.1 e 2.2      | *Personas* e *Casos de Uso*   |
| Arquitetura              | 3.2            | *Fluxos Alternativos*           |
| Tecnologias              | 3.3            | **não existe**             |
| Segurança               | 3.4            | **não existe**             |
| Normas e legislações   | 3.5            | **não existe**             |

Numeração real em `documentation/RFC/modelo-de-RFC.md`: 1 Visão do Produto · 2 Engenharia de Requisitos · 3 Fluxos · 4 Mockups/UX · 5 Arquitetura (5.1 C4, 5.2 Dados, 5.4 Stack) · 6 Segurança (6.1 LGPD) · 7 Planejamento.

**Impacto:** o avaliador não encontra o que foi mandado avaliar. Provável causa: o RFC foi renumerado (commits `bb28213`, `390b1a5`) sem atualizar as diretrizes.

### C2. O template de RFC não tem campo de nota, mas a diretriz exige nota — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:35` × `documentation/RFC/modelo-de-RFC.md:532-553`

> **Resolução:** a Seção 10 do template foi reconstruída. Cada avaliador agora tem uma ficha com
> **Nome · Nota (0–10, passo 0,5) · Situação (Aprovada / Aprovada com correções / Reprovada) · Data ·
> Assinatura**, mais lista numerada de **correções obrigatórias** e espaço para comentários.
> Foi acrescentado um bloco de **Consolidação** com as três notas, a média final, as correções
> consolidadas e o campo de validação pelo professor da disciplina. A tabela de faixas
> (7,0+ / 6,0–6,5 / <6,0) foi replicada no topo da seção para o avaliador não precisar consultar outro documento.

Registro do problema original:

Diretriz: *"Cada professor atribuirá **uma nota única** de 0 a 10 (intervalos de 0,5) e assinará no próprio RFC"* — com tabela de escala de 10 a <6.
Template Seção 10 (Parecer do Comitê): só `[ ] Aprovado  [ ] Ajustar`. **Não há campo de nota nem de assinatura.**

A regra é literalmente impossível de cumprir com o template atual.

### C3. Repositório `The-Portfolio-Playbook-II` está morto (HTTP 404) — ✅ **RESOLVIDO em 25/07/2026**

`disciplina-portfolio.md:16-20, 45-47` — 8 links

> **Resolução:** os 8 links estavam todos em `disciplina-portfolio.md`, que foi **removido do repositório**
> (ver M1). Nenhuma referência a `The-Portfolio-Playbook-II` sobrou em nenhum arquivo.

Registro do problema original:

Todos apontam para `github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook-II`, que retorna **404**. Vários ainda apontam para uma branch `working` inexistente. Nenhum desses links abre.

### C4. Link do modelo de RFC quebrado no PAC VII — ✅ **RESOLVIDO em 25/07/2026**

`PAC Extensionista VII.md:85`

Apontava para `documentation/modelo-de-RFC.md` — arquivo inexistente. Corrigido para `documentation/RFC/modelo-de-RFC.md`, agora idêntico ao link da linha 67.

### C5. Link do Portfólio Directions quebrado nas diretrizes — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:9`

Apontava para `portfolio-directions.md` na raiz. Corrigido para `directions/portfolio-directions-GERAL.md`.

### C6. Segundo link quebrado do RFC nas diretrizes — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:64`

Apontava para `The-Portfolio-Playbook-I/blob/main/modelo-de-RFC.md`. Corrigido para o caminho real no repositório atual. O link do cabeçalho (linha 7), que apontava para a raiz do repo antigo, também foi redirecionado para `PAC Extensionista VII.md`.

**Verificação:** os 5 caminhos internos referenciados em `diretrizes-avaliacao-professores.md`, `modelo-de-RFC.md` e `PAC Extensionista VII.md` foram checados contra o sistema de arquivos — todos resolvem.

### C7. Peso da nota final do Demo Day: dois cálculos diferentes — ✅ **RESOLVIDO em 25/07/2026**

`Portfolio.md:63-65` × `demoday/Avaliacao_Poster_DemoDay.md:12, 151, 157`

> **Resolução:** o professor confirmou que **90% professores / 10% comunidade** é a regra correta.
> `demoday/Avaliacao_Poster_DemoDay.md` foi corrigido nas linhas 10-12, 151 e 157 para explicitar os pesos
> e a média ponderada. Os dois documentos agora dizem a mesma coisa.
> A conversão Likert 1-5 → nota 0-10 foi fechada em seguida, em **C8**.

Registro do problema original:

- `Portfolio.md`: 3 professores = **90%**, comunidade = **10%**, média **ponderada**.
- `Avaliacao_Poster_DemoDay.md:12`: *"A média das notas atribuídas resultará em uma única nota final"* → média **simples** de 4 notas ⇒ comunidade valeria **25%**.
- `Avaliacao_Poster_DemoDay.md:151`: *"peso menor"* (sem número).
- `Avaliacao_Poster_DemoDay.md:157`: *"média ponderada"* (sem número).

O mesmo evento tem duas fórmulas de nota. O documento de avaliação (o que os professores usam no dia) é o que está errado/vago.

### C8. Escala Likert 1–5 sem regra de conversão para a nota 0–10 — ✅ **RESOLVIDO em 25/07/2026**

`demoday/Avaliacao_Poster_DemoDay.md:20-28, 155-158`

> **Resolução:** adotada a conversão **média dos 6 critérios × 2**. A seção *“Como a Likert vira nota”*
> foi acrescentada ao `Avaliacao_Poster_DemoDay.md` com o passo a passo, um exemplo numérico completo
> e três observações: piso de 2,0, critério 5 eliminatório e peso igual entre os 6 critérios.

Registro do problema original:

Os 6 critérios são pontuados em Likert de 1 a 5. A nota final é de 0 a 10. **Não existe fórmula de conversão documentada** (média × 2? soma? média ponderada por critério?). Dois professores podem calcular notas diferentes com as mesmas percepções.

---

## 🟠 ALTO — regras que se contradizem

### A1. Existe banca ou não? — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** decidido que **as três datas de dezembro SÃO o Poster + Demo Day** — o evento é a banca
> avaliadora da disciplina, em formato de apresentação aberta. `Portfolio.md:5` deixou de dizer que o Demo Day
> “substitui o modelo tradicional de banca” e passou a nomeá-lo como a própria banca. A seção *Datas e Prazos*
> e a nota sobre os professores de Joinville foram reescritas com o mesmo nome.
> Permanece separada a **Banca Técnica Especial**, exclusiva dos projetos de destaque (ver A2).

Registro do problema original:

- `Portfolio.md:5` e `disciplina-portfolio.md:7`: Demo Day *"substitui o modelo tradicional de banca"*.
- `Portfolio.md:72`: existe **Banca Técnica Especial**, só para destaques.
- `Portfolio.md:74-78`: **3 datas de banca** (10, 15 e 16/12/2026) aparentemente para todos.

Três definições de "banca" convivendo no mesmo arquivo.

### A2. Nome do evento de destaque muda em cada documento — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** padronizado **“Banca Técnica Especial”**. A menção a *“Seminário e Artigo”* foi removida
> do `iot.md` — destaque rende menção e convite à banca, sem produção de artigo. O nome agora aparece
> igual nos seis arquivos (Portfolio.md + as cinco directions).

Registro do problema original:

| Documento                                     | Nome                                          |
| --------------------------------------------- | --------------------------------------------- |
| `Portfolio.md:72`                           | Banca Técnica Especial                       |
| `disciplina-portfolio.md:31-32`             | Noite de Destaques + banca técnica convidada |
| `directions/portfolio-directions-iot.md:60` | Banca Técnica / Seminário e Artigo          |

### A3. Repositório privado é permitido em Jogos e proibido em todo o resto — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** decidido **abrir exceção explícita para Jogos Digitais**. `PAC Extensionista VII.md` e
> `Portfolio.md:14` agora registram a exceção e o motivo (assets licenciados, publicação em loja),
> exigindo acesso autorizado aos avaliadores. `portfolio-directions-jogosdigitais.md` passou a dizer
> que é a **única** linha com essa permissão.

Registro do problema original:

- `directions/portfolio-directions-jogosdigitais.md:6`: *"repositório público **ou privado** com acesso autorizado"*.
- `PAC Extensionista VII.md:19`: *"o repositório deve permanecer de acesso público"*.
- `PAC Extensionista VII.md:26`: *"disponibilizada em repositório de acesso público"*.
- `Portfolio.md:14`: *"Repositório **público** no GitHub"*.

### A4. CI/CD: obrigatório geral, desejável em Mobile, ausente em IA/IoT/Jogos — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução (A4, A5, A7 e A14 em conjunto):** adotado o modelo **núcleo comum + cobertura por linha**.
> Foi criada a seção *Núcleo comum de engenharia* em `ia.md`, `iot.md` e `jogosdigitais.md`, e os itens
> faltantes foram acrescentados em `webapp.md` e `mobile.md`. Wiki, CI/CD, análise estática e
> observabilidade agora são obrigatórios nas **cinco** linhas. Em Mobile, CI/CD subiu de desejável
> para obrigatório. Metas de cobertura por linha: Web 75/25 · Mobile 75/25 · IA 70% · IoT 60% · Jogos 50%.

Registro do problema original:

- `directions/portfolio-directions-GERAL.md:61`: Deploy via CI/CD = 🔑 **Obrigatório**.
- `directions/portfolio-directions-webapp.md:12`: obrigatório. ✅
- `directions/portfolio-directions-mobile.md:31`: listado como **desejável**. ❌
- IA, IoT e Jogos: **não mencionam CI/CD**. ❌

### A5. TDD: obrigatório geral, ausente em 3 das 5 linhas — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** ver A4 — tratado no mesmo pacote. Cada linha passou a ter meta de cobertura própria.

Registro do problema original:
`directions/portfolio-directions-GERAL.md:62` marca TDD como 🔑 Obrigatório. Só webapp (18-20) e mobile (18-20) exigem cobertura (75% back / 25% front). IA, IoT e Jogos não citam testes automatizados nem cobertura.

### A6. Mobile se contradiz internamente sobre testes — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** a duplicata foi removida. A linha *desejável* passou a tratar de **testes instrumentados**
> (execução em dispositivo/emulador), que é coisa distinta dos testes unitários obrigatórios.

Registro do problema original:
`directions/portfolio-directions-mobile.md:18-20` exige testes unitários com TDD e cobertura como **obrigatório**; a linha 32 lista *"Aplicação de testes automatizados (unitários ou instrumentados)"* como **desejável**. O mesmo requisito nos dois níveis.

### A7. Documentação em Wiki: obrigatória e nunca mais citada — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** ver A4 — Wiki foi propagada como obrigatória para as cinco linhas.

Registro do problema original:
`directions/portfolio-directions-GERAL.md:60` marca Wiki do GitHub como 🔑 **Obrigatório**. Nenhuma das 5 linhas de projeto menciona Wiki, e `Portfolio.md:17` fala apenas em "documentação de arquitetura, requisitos e decisões técnicas". Requisito obrigatório que não chega ao aluno.

### A8. Vercel: proibido nas directions, exemplo positivo na avaliação — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** o exemplo em `Avaliacao_Poster_DemoDay.md:138` foi trocado por nuvem, servidor
> institucional, loja ou build pública. Foi acrescentada a nuance real: plataformas focadas em frontend
> (Vercel, Netlify, Render) **são aceitas quando há backend próprio** — o veto nunca foi ao produto,
> e sim ao seu uso como substituto do backend.

Registro do problema original:

- `directions/portfolio-directions-GERAL.md:38`: ⚠️ Evitar.
- `directions/portfolio-directions-webapp.md:66`: "deve ser evitado".
- `demoday/Avaliacao_Poster_DemoDay.md:138`: *"Exemplo: link público via **Vercel**, Firebase ou servidor institucional"* — como **exemplo de boa demonstração funcional**.

O professor avalia positivamente aquilo que a direction penaliza.

### A9. Firebase / Supabase: desejável em Mobile, evitado no GERAL, proibido em Web — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** Firebase e Supabase foram **retirados** das listas de desejáveis do `mobile.md`.
> A linha de persistência passou a citar apenas armazenamento local no dispositivo
> (SQLite, RealmDB, DataStore) e a de integração externa deixou de listar Firebase.
> Mobile ficou alinhado ao veto a BaaS do `GERAL.md:39` e do `webapp.md:66-67`.

Registro do problema original:

- `directions/portfolio-directions-mobile.md:35`: Firebase e Supabase como persistência **desejável**.
- `directions/portfolio-directions-GERAL.md:39`: plataformas BaaS = ⚠️ Evitar.
- `directions/portfolio-directions-webapp.md:66-67`: Firebase citado como hospedagem a evitar e BaaS como "no-code disfarçado".

### A10. SQLite: proibido no GERAL/Web, desejável em Mobile — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** ambiguidade explicitada. `mobile.md` ganhou nota dizendo que o veto a banco em disco vale
> para o **banco de produção do backend**; persistência local no dispositivo (cache, offline, preferências)
> é prática esperada e não incorre no veto. Firebase e Supabase saíram dessa lista (ver A9).

Registro do problema original:
`directions/portfolio-directions-GERAL.md:29` e `webapp.md:83` proíbem banco em disco (H2, SQLite). `mobile.md:35` lista SQLite como desejável. Pode ser intencional (persistência local em app), mas **não está explicitado** — lê-se como contradição.

### A11. Scrum evitado nas directions, sprints exigidas no PAC VIII — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** `PAC Extensionista VIII.md:13` passou de “planejar as *sprints*” para “planejar as
> *iterações* de entrega”, removendo o vocabulário de Scrum sem perder o sentido.

Registro do problema original:

- `directions/portfolio-directions-GERAL.md:37`: Scrum = ⚠️ Evitar, *"não indicada para projetos individuais"*.
- `PAC Extensionista VIII.md:13`: *"O aluno utiliza este espaço para planejar as **sprints**"*.

### A12. Ambiente produtivo em nuvem: exigido no geral, incompatível com Jogos — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** definido que, em Jogos, **build pública e distribuída conta como ambiente produtivo**
> (Itch.io, loja, WebGL hospedado ou APK). A exceção foi escrita nos dois lados — `Portfolio.md:20` e
> `jogosdigitais.md` — com o limite explícito: não vale build que só roda na máquina do autor.
> A lacuna de IoT foi fechada em separado, exigindo hospedagem pública da camada de aplicação.

Registro do problema original:

- `Portfolio.md:20`: deve estar *"hospedado na nuvem, com acesso público e estável (sem depender de notebook pessoal ou ambiente local)"*.
- `directions/portfolio-directions-jogosdigitais.md:5`: aceita *"executável standalone"* — que não é ambiente produtivo em nuvem.
- IoT (`iot.md:11-14`) exige internet e camada de aplicação, mas nunca fala em hospedagem pública.

### A13. Régua de Avaliação existe em 3 linhas e não existe em 2 — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** as **cinco** linhas passaram a ter *Régua de Avaliação* no mesmo vocabulário —
> **Destaque / Aprovado / Reprovado**. Réguas criadas em `webapp.md` e `mobile.md`; as de IA, IoT e Jogos
> foram reescritas no padrão. Todas ancoram em **nota final ≥ 6,0** e no núcleo comum de engenharia,
> e todas apontam o Destaque para a Banca Técnica Especial.

Registro do problema original:
IA (`ia.md:59-62`), IoT (`iot.md:55-61`) e Jogos (`jogosdigitais.md:50-53`) têm "Régua de Avaliação". **Web Apps e Mobile não têm.** Além disso o vocabulário difere: IA/Jogos usam *Aprovado / Destaque / Reprovado*; IoT usa *Aprovado para apresentação / Aprovado com Diferencial / não aprovado*.

### A14. Análise estática e observabilidade: obrigatórias só em 2 linhas — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** ver A4 — ambas propagadas para as cinco linhas.

Registro do problema original:
Exigidas em `webapp.md:21-22` e `mobile.md:21-22`, e preferidas em `GERAL.md:44-45`. Ausentes de IA, IoT e Jogos, embora `Portfolio.md:43` coloque observabilidade como pilar de DevOps para todos.

### A15. Termo de aceite do parceiro é obrigatório, mas nem todo aluno tem parceiro — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a Seção **3.1 — Modalidade Comunidade: evidência equivalente** no
> `PAC Extensionista VIII.md`, com quatro evidências de mesmo peso (relatório de validação com ao menos
> três sessões, feedback documentado, declaração da comunidade atendida e registro das correções).
> O NP3 e a lista de entregáveis foram atualizados. A modalidade deve ser declarada no início do semestre.

Registro do problema original:
`PAC Extensionista VIII.md:46, 57` exige *"Termo de aceite ou declaração de encerramento assinado pelo parceiro externo"* no NP3 (60% da nota). Mas `PAC Extensionista VII.md:21-26` permite explicitamente a modalidade **"Projetos voltados à Comunidade"**, sem parceiro corporativo. Para esses alunos não há de quem obter o termo — a regra não prevê o caso.

### A16. O Demo Day é avaliado nas duas disciplinas sem separação de critérios — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** separado **por dimensão**. O NP3 do PAC VIII deixou de pontuar “apresentação técnica no
> Demo Day” e passou a pontuar a **socialização extensionista** — evidência de que a solução foi devolvida
> ao parceiro ou à comunidade. Foi acrescentada nota explicitando a divisão: Portfólio avalia produto e
> apresentação técnica; PAC VIII avalia o que o parceiro recebeu, validou e passou a usar.

Registro do problema original:
`PAC Extensionista VIII.md:47` põe *"Socialização: Apresentação técnica no Demo Day"* dentro do NP3 (60%). `Portfolio.md:61-65` e o critério 6 de `Avaliacao_Poster_DemoDay.md:128-144` avaliam a mesma apresentação. Não há regra dizendo o que cada disciplina pontua — risco de dupla contagem ou de nota conflitante.

### A17. Limiar de aprovação do RFC é ambíguo — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:37, 42, 44-53`

> **Resolução:** o professor definiu **6,0 como nota mínima de aprovação**, com uma faixa condicional:
> entre **6,0 e 7,0** a validação pode ser condicionada a **correções obrigatórias** — sem elas a proposta
> perde sustentação, a nota cai abaixo de 6,0 e reprova. Abaixo de 6,0, reprovada direto.
>
> A seção *Registro da Avaliação* e o *Anexo - Escala* foram reescritos: limiar explícito em ambos,
> coluna **Situação** (✅ Aprovada / ⚠️ Aprovada com correções / ❌ Reprovada), degrau **9,5** incluído,
> **6** separado de **6,5** e nota de rodapé explicando a faixa condicional. A tabela agora cobre
> todos os degraus de 0,5 sem lacuna.

Registro do problema original:

- Texto: *"Notas **abaixo de 7** indicam necessidade de ajustes obrigatórios"*.
- Tabela: **7** = "Limite para aprovação", **6 e 6.5** = "Revisar", **abaixo de 6** = "Reapresentar" (reprovada).

Três faixas negativas com nomes diferentes e nenhuma diz claramente se 7 aprova. A tabela também **pula o 9.5** e agrupa 6 com 6.5 numa linha só, quebrando o passo de 0,5 declarado.

---

## 🟡 MÉDIO — terminologia, estrutura e lacunas

### M1. `disciplina-portfolio.md` é um documento órfão e desatualizado — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** arquivo **removido** (`git rm`). Comparação seção a seção confirmou que todo o conteúdo
> já estava coberto — e em versão mais rigorosa — por `Portfolio.md`, `demoday/guia_poster.md`,
> `directions/` e `PAC Extensionista VII.md`. Os três bullets de *Participação no Poster + Demo Day*
> eram texto idêntico ao de `guia_poster.md:3-7`.
>
> Quatro pontos existiam apenas nele — o nome *“Noite de Destaques”*, a composição da banca convidada
> (professores, profissionais do mercado e especialistas da área), a possível integração com a
> **Semana Acadêmica** e *“apresentação”* como quarto critério de destaque. O professor decidiu
> **suprimir os quatro**, sem merge para o `Portfolio.md`.
>
> O arquivo permanece recuperável pelo histórico do Git. As modificações locais descartadas eram
> apenas de formatação (linhas em branco antes de listas) mais um `o ` digitado por engano na linha 1.

Registro do problema original:
Descreve a mesma disciplina que `Portfolio.md`, com conteúdo divergente e inferior: todos os links mortos (repo `-II`), *"critérios a ser definido em documento específico"*, "Noite de Destaques" em vez de "Banca Técnica Especial", requisitos de entrega mais fracos (sem CI/CD, sem quatro orientações, sem ambiente produtivo). **Nenhum documento do repositório aponta para ele** — o `README.md:18` linka apenas `Portfolio.md`. Candidato a remoção ou fusão.

### M2. RFC oferece duas linhas de projeto que não existem — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** o campo *Linha de Projeto* do RFC passou a listar exatamente as **cinco linhas oficiais**
> (Web Apps / Mobile / Jogos Digitais / IA / IoT), com link para o Portfólio Directions.
> “Plataforma” e “Dados” foram removidas.

Registro do problema original:
`documentation/RFC/modelo-de-RFC.md:13` oferece *"Web / Mobile / IA / IoT / Jogos / **Plataforma / Dados**"*. Só existem **cinco** linhas oficiais (`PAC Extensionista VII.md:42`, `GERAL.md`, `disciplina-portfolio.md`). "Plataforma" e "Dados" são linhas fantasma sem direction, sem régua e sem critérios.

### M3. Projeto é individual, mas 3 documentos falam em "equipe" / "grupo" — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** `Avaliacao_Poster_DemoDay.md` passou de “a equipe demonstra segurança” para “o autor”;
> `webapp.md` de “desenvolvido pelo grupo” para “pelo aluno”; `Portfolio.md` de “Título, autores e e-mails”
> para “Título, autor e e-mail”. A quarta ocorrência saiu com o `disciplina-portfolio.md`.

Registro do problema original:
`PAC Extensionista VII.md:32` e `guia_poster.md:21` deixam claro que é individual. Contradizem:

- `demoday/Avaliacao_Poster_DemoDay.md:140`: *"**equipe** demonstra segurança ao responder perguntas"*.
- `directions/portfolio-directions-webapp.md:66`: *"sem backend desenvolvido pelo **grupo**"*.
- `Portfolio.md:53`: pôster deve conter *"Título, **autores** e e-mails"* (plural).

### M4. GDD Template: numeração duplicada — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** seções renumeradas. O documento agora vai de **1 a 19** sem repetição:
> 12 Arquitetura · 13 Testes e Playtests · 14 Cronograma · 15 Riscos · 16 Limitações · 17 Decisões ·
> 18 Créditos · 19 Reflexão Final. Verificado programaticamente.

Registro do problema original:
`documentation/games/GDD - Template.md`

- `# 12` aparece duas vezes: *Arquitetura de Software* (linha 246) e *Testes e Playtests* (linha 269).
- `# 17` aparece duas vezes: *Créditos* (linha 326) e *Reflexão Final* (linha 337).

O documento vai de 1 a 17 com dois números repetidos — na prática são 19 seções.

### M5. GDD Template e Guia de Preenchimento têm estruturas diferentes — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** decidido que **vale o template**. O `GuiaPreenchimenteBoasPraticas.md` foi **reescrito**
> para seguir a mesma numeração e os mesmos títulos das 19 seções — verificado programaticamente,
> **19/19 alinhadas**. O conteúdo do guia antigo foi redistribuído nas seções correspondentes e foram
> escritas as seis que faltavam (Hipóteses de Design, Escopo, Prototipagem, Cronograma, Riscos e Decisões).
> A seção *Narrativa*, que existia só no guia, foi absorvida como item opcional da Seção 1.
>
> De carona, dois títulos do template que carregavam instrução — `# 10. Áudio (tabela/onde usar/loop/descrição)`
> e o equivalente em Animação — foram limpos, com a instrução e a tabela-exemplo movidas para o corpo.

Registro do problema original:
O guia diz (linhas 7-16) que explica "como preencher cada seção do template", mas usa outra estrutura:

**Só no guia:** Informações Gerais · Conceito e Visão · Narrativa e Contexto · Documentação Visual · Engenharia de Software e Qualidade · Recomendações Gerais
**Só no template:** Hipóteses de Design · Pilares do jogo · Prototipagem · Escopo do Projeto · Camera · Animação · Cronograma · Riscos do Projeto · Decisões Importantes

Não existe mapeamento seção↔seção. O aluno não consegue usar o guia para preencher o template.

### M6. "Elevated Pitch" × "Elevator Pitch" — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** `GDD - Template.md` corrigido para **Elevator Pitch**, alinhado ao guia.

Registro do problema original:
`GDD - Template.md:18` escreve **Elevated Pitch**; `GuiaPreenchimenteBoasPraticas.md:111` escreve **Elevator Pitch** (correto).

### M7. GDD é obrigatório ou desejável? — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** separados os dois níveis. O **GDD mínimo** (visão, loop, mecânicas, tecnologias) é
> obrigatório e agora aponta para o template oficial; o **GDD completo**, com hipóteses, prototipagem,
> riscos e decisões, permanece desejável.

Registro do problema original:
`directions/portfolio-directions-jogosdigitais.md:7` exige *"Documentação com foco em game design"* como **obrigatório**; a linha 15 põe *"Documento de Game Design (GDD) estruturado... GDD Completo"* como **desejável**. Existe um template oficial de GDD no repositório, o que sugere obrigatoriedade.

### M8. A linha de Jogos não linka o template nem o guia de GDD — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** `portfolio-directions-jogosdigitais.md` passou a linkar o **Template de GDD** e o
> **Guia de Preenchimento** no item obrigatório de documentação. Os dois arquivos deixaram de ser órfãos.

Registro do problema original:
`directions/portfolio-directions-jogosdigitais.md` nunca referencia `documentation/games/GDD - Template.md` nem `GuiaPreenchimenteBoasPraticas.md`. Os dois arquivos de games são órfãos — nenhum documento do repositório aponta para eles.

### M9. WCAG é cobrado na avaliação e não existe nas normas — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** **WCAG 2.1** foi acrescentada à tabela de `normas.md` como norma **Core**, com aplicação
> prática (contraste, navegação por teclado, texto alternativo, semântica) e links para a norma e para o
> guia rápido do W3C.

Registro do problema original:
`documentation/diretrizes-avaliacao-professores.md:29` manda avaliar aderência a *"LGPD, **WCAG**, HIPAA"*. `documentation/normas.md` **não lista WCAG** na tabela (só cita "acessibilidade" en passant na linha 27). Norma cobrada sem estar documentada.

### M10. Classificação "Core" das normas contradiz o próprio texto — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a categoria **Setorial** e acrescentada legenda explicando as três:
> *Core* (vale para praticamente todo projeto), *Setorial* (obrigatória só no domínio indicado) e
> *Complementares* (boas práticas de referência). HIPAA, ESRB/PEGI e Prontuário Eletrônico migraram
> para Setorial. A tabela ficou 3 / 3 / 3.

Registro do problema original:
`documentation/normas.md:15-16`

- **HIPAA** marcada como **Core**, mas a descrição diz *"Relevante para projetos com usuários, clínicas ou hospitais **dos EUA**"*.
- **ESRB / PEGI** marcada como **Core**, mas só se aplica a jogos digitais.

Core deveria significar "aplica-se a todos". Do jeito atual, LGPD (universal) e HIPAA (nicho) estão no mesmo nível.

### M11. "Prova de autoria" não está definida em lugar nenhum — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a seção **Prova de Autoria** no `Portfolio.md`. É o **último encontro da disciplina**,
> individual, no qual o professor questiona o aluno sobre o trabalho — conhecimento do codebase, decisões
> de engenharia e domínio do que foi construído. Ficou registrado que a aprovação é **condição para
> habilitar-se ao Demo Day**, que ela não avalia a qualidade do produto (isso é papel do Demo Day) e que
> o uso de assistentes de IA não é proibido, mas não dispensa o domínio do resultado.

Registro do problema original:
`Portfolio.md:70` estabelece que até 30/11/2026 o trabalho deve ter sido **aprovado na prova de autoria**. Nenhum documento define o que é, como é aplicada, quem aplica, o que acontece em caso de reprovação, ou se há segunda chance. `Avaliacao_Poster_DemoDay.md:116-124` trata autoria como critério de nota, não como gate eliminatório.

### M12. As "quatro orientações obrigatórias" não têm avaliação associada — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** o professor decidiu tratar as orientações como **gate**, não como item de nota, e
> ampliou o requisito. A regra passou a ser **seis participações obrigatórias**: **cinco orientações**
> (presenciais ou remotas), das quais **duas até 30/09/2026 (quarta-feira)** e as cinco até
> **30/11/2026 (segunda-feira)**, mais **uma participação como visitante** em noite do Poster + Demo Day
> distinta daquela em que o aluno apresenta, com **avaliação ativa dos trabalhos dos colegas**.
>
> Os dois gates ficaram separados por momento, porque a visita só é verificável durante o evento —
> depois do prazo de entrega:
>
> - **Habilitação para apresentar** (até 30/09 e 30/11): orientações + prova de autoria + requisitos de entrega.
> - **Aprovação na disciplina** (durante o evento): visita como visitante + avaliação dos colegas.
>
> Criada a seção **Requisitos de Aprovação** em `Portfolio.md`, com tabela de prazos por condição e os
> três blocos (habilitação · participação no evento · nota ≥ 6,0). A regra foi propagada para
> `demoday/Avaliacao_Poster_DemoDay.md` § *Participação da Comunidade Acadêmica* — explicitando que os
> alunos da disciplina **integram** a comunidade que gera os 10% e que avaliar é obrigatório para eles —
> e para `demoday/guia_poster.md` § *Participação no Poster + Demo Day*. O **registro de presença** já
> previsto em `Portfolio.md` § *Datas e Prazos* foi nomeado como a comprovação da visita.

Registro do problema original:

`Portfolio.md:13` exige *"Participação de quatro orientações presenciais ou remotas"* com evidência. Nenhum outro documento menciona isso, e não há critério, peso ou consequência definida no `Avaliacao_Poster_DemoDay.md`.

### M13. Lista de conteúdo do pôster diverge entre dois documentos — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** a lista do `Portfolio.md` foi completada com os três itens que só existiam no guia —
> **logomarca**, **referências** e **template oficial** — mais um ponteiro para o Guia do Pôster como
> fonte da lista completa e do checklist.

Registro do problema original:

| `Portfolio.md:53-57`        | `demoday/guia_poster.md:18-28`        |
| ----------------------------- | --------------------------------------- |
| Título, autores, e-mails     | Título, nome e e-mail do integrante    |
| Contexto, problema, solução | Contexto/Problema, Solução            |
| Arquitetura                   | Arquitetura                             |
| QR Code                       | QR Code                                 |
| —                            | **Logomarca da Católica SC**     |
| —                            | **Referências**                  |
| —                            | **Template obrigatório (.pptx)** |

Três elementos obrigatórios do guia não aparecem na lista do `Portfolio.md`.

### M14. PAC VIII não tem prazo de entrega — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a seção **Prazos** no `PAC Extensionista VIII.md`, com a entrega final em
> **30/11/2026 (segunda-feira)** — mesmo prazo do Portfólio —, as três datas do Demo Day e o lembrete
> de declarar a modalidade no início do semestre.

Registro do problema original:
`Portfolio.md:70` e `PAC Extensionista VII.md:77` têm 30/11/2026. `PAC Extensionista VIII.md` — mesma fase, mesmo semestre, NP3 com entrega final — **não tem nenhuma data**.

---

## ⚪ BAIXO — links stale, formatação e digitação

### B1. 20 links apontam para o repositório antigo `The-Portfolio-Playbook-I` — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** **16 links** substituídos pelo nome atual do repositório em 4 arquivos
> (`Portfolio.md`, `PAC Extensionista VII.md`, `GERAL.md`, `guia_poster.md`). Os 11 caminhos únicos
> foram conferidos antes: todos existiam, só o nome do repo estava velho.
> **Verificação final:** 41 links internos checados contra o sistema de arquivos, **0 quebrados**,
> nenhuma referência a `-I` ou `-II` remanescente.

Registro do problema original:
Retorna **HTTP 301** e redireciona para `The-Portfolio-Playbook` (este repo). Funcionam, mas são frágeis. Arquivos afetados: `Portfolio.md:19,79-81`, `directions/portfolio-directions-GERAL.md:5-17`, `demoday/guia_poster.md:27-28`, `documentation/diretrizes-avaliacao-professores.md:7,9,64`, `disciplina-portfolio.md:44`.

**Recomendação:** padronizar tudo em links relativos (`./directions/...`), que sobrevivem a renomeação de repositório e funcionam no GitHub e em clones locais.

### B2. Tabela quebrada no GERAL.md — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** a linha do TDD ganhou o `|` de fechamento. A tabela volta a renderizar por completo.

Registro do problema original:
`directions/portfolio-directions-GERAL.md:62` — a linha do TDD não fecha a última coluna com `|`, quebrando a renderização da tabela a partir daquele ponto.

### B3. `documentation/normas.md:21` — linha de espaços em branco soltos logo após a tabela. — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** linha removida.

Registro do problema original:

### B4. `disciplina-portfolio.md:48-60` — 13 linhas em branco seguidas antes de um `---` solto no fim do arquivo. — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** sem efeito — o arquivo foi removido do repositório (ver M1).

Registro do problema original:

### B5–B11. Erros de digitação — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** todos os typos de conteúdo foram corrigidos — `requisitros`, `comuidade`,
> `acdêmico`, `necessáriamente`, `conrtole`, `hospedaagem`, `protocolo enter`, `inpiram`,
> `Todos as animações usadas eonde`. Os de `disciplina-portfolio.md` saíram com o arquivo.
>
> **Nome dos arquivos:** `TEMPLATE_POSTER_PORTIFOLIO.pptx` e `.pdf` foram renomeados para
> **PORTFOLIO** via `git mv` (histórico preservado), com os links do `guia_poster.md` atualizados.
> O semestre está começando e não havia URLs em circulação.

Registro do problema original:

| Arquivo:linha                                   | Erro                                           | Correto                            |
| ----------------------------------------------- | ---------------------------------------------- | ---------------------------------- |
| `Portfolio.md:19`                             | requisitros                                    | requisitos                         |
| `PAC Extensionista VII.md:3`                  | comuidade                                      | comunidade                         |
| `disciplina-portfolio.md:41`                  | reqisitos defindos                             | requisitos definidos               |
| `demoday/Avaliacao_Poster_DemoDay.md:122`     | acdêmico                                      | acadêmico                         |
| `demoday/guia_poster.md:28`                   | necessáriamente                               | necessariamente                    |
| `directions/portfolio-directions-GERAL.md:39` | conrtole                                       | controle                           |
| `directions/portfolio-directions-GERAL.md:40` | hospedaagem                                    | hospedagem                         |
| `directions/portfolio-directions-GERAL.md:59` | protocolo enter aplicações                   | protocolo entre aplicações       |
| `documentation/games/GDD - Template.md:242`   | Todos as animações usadas eonde              | Todas as animações usadas e onde |
| `documentation/games/GDD - Template.md:72`    | inpiram                                        | inspiram                           |
| `demoday/` (nome de arquivo)                  | TEMPLATE_POSTER_**PORTIFOLIO**.pptx/.pdf | PORTFOLIO                          |

### B12. Datas fora do padrão recém-adotado — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** `GDD - Template.md` passou a usar `DD/MM/AAAA` nas tabelas de playtests e de decisões
> (antes `DD/MM` e “março”/“abril”). A data de 2024-1 nas diretrizes saiu junto com o B13.

Registro do problema original:
Padrão do projeto: `DD/MM/AAAA` + dia da semana. Fora do padrão:

- `documentation/games/GDD - Template.md:275-276` — tabela de playtests usa `DD/MM`.
- `documentation/games/GDD - Template.md:321-322` — decisões datadas como "março" / "abril".
- `documentation/diretrizes-avaliacao-professores.md:3` — "semestre 2024-1".

### B13. Diretrizes de avaliação estão dois anos defasadas — ✅ **RESOLVIDO em 25/07/2026**

`documentation/diretrizes-avaliacao-professores.md:3` falava em *"início do semestre 2024-1"* e usava a nomenclatura **Portfólio I / Portfólio II**. Parágrafo reescrito com a estrutura atual (PAC Extensionista VII · PAC Extensionista VIII · Disciplina de Portfólio) e sem referência a semestre específico, para não envelhecer de novo.

### B14. README não dá acesso a metade do repositório — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a seção **📚 Documentos de apoio** no `README.md`, com links para as cinco
> directions, os três documentos do Demo Day, o modelo de RFC, as diretrizes de avaliação, as normas
> e os dois documentos de games. Links relativos, validados contra o sistema de arquivos.

Registro do problema original:
`README.md` linka apenas os 3 documentos de disciplina. Não há caminho de navegação para `directions/`, `demoday/`, `documentation/normas.md`, o modelo de RFC ou os documentos de games.

---

# 🔁 Segunda rodada de auditoria — 25/07/2026

**Escopo:** os 20 documentos versionados, relidos integralmente após o fechamento dos 47 itens da
primeira rodada. **Método:** extração mecânica de números, datas, porcentagens, terminologia e simetria
estrutural + releitura cruzada. **Resultado: 22 itens novos**, nenhum deles detectável pelos checks
automatizados da primeira rodada (que só validavam links e numeração).

| Severidade | Itens | Resolvidos | Abertos |
|---|---|---|---|
| 🔴 Crítico | 2 | 0 | **2** |
| 🟠 Alto | 6 | 0 | **6** |
| 🟡 Médio | 8 | 0 | **8** |
| ⚪ Baixo | 6 | 0 | **6** |
| **Total** | **22** | 0 | **22** |

## 🔴 CRÍTICO — dois documentos dão veredictos opostos sobre o mesmo projeto

### C9. O critério de nota não exige a cobertura de testes que a linha exige — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** o professor tirou a cobertura do campo de nota e a transformou em **gate**, conferido na
> **prova de autoria**, reaproveitando o mecanismo definido no **A22**: não atingindo o mínimo, o aluno
> **corrige** — escreve os testes que faltam — e tem **uma segunda tentativa**; reprovando na segunda,
> **reprova na disciplina** e não chega ao evento.
>
> A contradição desaparece porque os dois documentos passam a falar de coisas diferentes:
>
> - **`Portfolio.md` § Prova de Autoria** ganhou a cobertura como quarto item verificado, com os números
>   por linha (75/25 · 70% · 60% · 50%).
> - **Critério 3** deixou de medir quantidade e passou a pontuar **qualidade e pertinência** dos testes,
>   com nota de rodapé dizendo que a cobertura é gate já conferido — *"todo trabalho que você avalia já
>   cumpriu a cobertura"*. Também passou a penalizar o inverso: testes rasos que só perseguem percentual.
> - A seção de **pré-condição** do documento de avaliação lista os dois gates e as segundas tentativas.
>
> Efeito colateral desejável: some o incentivo a inflar cobertura com testes vazios, porque o percentual
> deixou de dar nota e a qualidade passou a dar.

Registro do problema original:

`demoday/Avaliacao_Poster_DemoDay.md:84-86` × `directions/portfolio-directions-*.md`

O critério **3 — Qualidade Técnica do Código** pede apenas *"presença de testes unitários e/ou de
integração"*, sem número. As directions fixam cobertura como item **obrigatório**: 75% backend / 25%
frontend (webapp, mobile), 70% (IA), 60% (IoT), 50% (Jogos).

**Impacto:** um projeto com 15% de cobertura pode receber Likert 4 no critério 3 e fechar nota 8,0,
enquanto a *Régua de Avaliação* da sua linha o classifica como **Reprovado** por descumprir item
obrigatório. Os dois documentos oficiais chegam a conclusões opostas, e o que o professor usa no dia do
evento é o que não menciona o número.

### C10. TDD é 🔑 Obrigatório no GERAL e não existe em três das cinco linhas

`directions/portfolio-directions-GERAL.md:62` × `ia.md:23`, `iot.md:25`, `jogosdigitais.md:22`

GERAL marca **TDD** como 🔑 Obrigatório, válido para todos. Apenas `webapp.md:18` e `mobile.md:18`
dizem *"Cobertura de testes unitários **com TDD**"*. IA, IoT e Jogos falam só em *"cobertura de testes
automatizados"* — que se atinge escrevendo testes depois do código.

**Nota:** o item **A5** foi marcado resolvido na primeira rodada, mas a correção não chegou a essas três
linhas. Reincidência, não achado novo.

## 🟠 ALTO — regras que se contradizem

### A18. "Banca" voltou a ter três significados

| Documento | Termo | Refere-se a |
|---|---|---|
| `Portfolio.md:5,98` | *"a banca avaliadora da disciplina"* | o Poster + Demo Day |
| `PAC Extensionista VII.md:77` | *"**Banca Avaliadora**"* | os três professores que avaliam a RFC |
| `documentation/RFC/modelo-de-RFC.md:532` | *"**Comitê de Avaliação**"* | os mesmos três professores da RFC |
| `Portfolio.md:150` + as 5 directions | *"**Banca Técnica Especial**"* | sessão dos projetos de destaque |

O **A2** padronizou o nome do evento de destaque, mas não o de "banca". Hoje *banca avaliadora* nomeia
duas coisas diferentes em dois documentos, e o corpo que avalia a RFC tem dois nomes.

### A19. Vercel e Netlify aparecem como exemplo positivo de CI/CD

`demoday/Avaliacao_Poster_DemoDay.md:102` × `:139` × `GERAL.md:38` × `webapp.md:67`

O critério 4 lista *"GitHub Actions, GitLab CI, Jenkins, **Vercel, Netlify**"* como exemplos de CI/CD,
sem ressalva. O **próprio arquivo**, 37 linhas abaixo (`:139`), diz que essas plataformas *"só são
aceitas quando há backend próprio desenvolvido pelo aluno"*. GERAL marca ⚠️ **Evitar** e `webapp.md:67`
coloca em *"o que não pode ter"*.

Mesma inconsistência do **A8**, sobrevivente num segundo ponto do mesmo arquivo.

### A20. O prazo do PAC VII é o mesmo do 8º semestre, e nenhum documento diz de que semestre se trata — 🟡 **PARCIALMENTE RESOLVIDO em 25/07/2026**

> **Resolução:** decidido que o **PAC VII tem calendário próprio**, do 7º período, sem compartilhar
> prazos com Portfólio e PAC VIII. O `30/11/2026` — que era a data do 8º período copiada para o
> documento do 7º — foi **removido**. No lugar entrou a seção **6. Prazos**, com tabela ancorada nas
> próprias NPs da disciplina (NP1 · NP2 · avaliação pelos três professores · NP3) e uma declaração
> explícita de que o calendário é independente.
>
> **Pendente:** as quatro datas estão marcadas *a definir*, com aviso no documento. Precisam do
> calendário do 7º período antes de publicar para a turma.

Registro do problema original:

`PAC Extensionista VII.md:79` × `Portfolio.md:100` × `PAC Extensionista VIII.md:66`

PAC VII (7º período) fixa entrega em **30/11/2026**. Portfólio e PAC VIII (8º período) fixam
**30/11/2026**. Se as duas disciplinas rodam no mesmo semestre-calendário com turmas diferentes, ambas
as datas estão certas — mas **nenhum documento declara o semestre ou a turma**, então o aluno lê o mesmo
prazo para duas disciplinas que o `README.md:12` descreve como sequenciais.

Agrava: o **B13** removeu deliberadamente *"semestre 2024-1"* das diretrizes para o texto não envelhecer.
As datas absolutas reintroduziram o envelhecimento **sem** trazer de volta a identificação da turma.

### A21. A linha Mobile herdou uma régua de cobertura que pode não se aplicar

`directions/portfolio-directions-mobile.md:18-20`

*"Cobertura de testes unitários com TDD: 75% no backend; 25% no frontend"* — texto idêntico ao de
`webapp.md:18-20`. Um app mobile pode não ter backend próprio (consumindo API de terceiros ou BaaS), e
nesse caso a meta obrigatória fica **indefinível**: 75% de um componente que não existe.

Falta a divisão adequada à linha — por exemplo lógica de domínio × camada de UI, como IA, IoT e Jogos
fizeram ao declarar o que fica fora da contagem.

> ⚠️ **Atenção ao corrigir:** desde a resolução do **C9**, os números de cobertura passaram a aparecer
> também em `Portfolio.md` § Prova de Autoria e em `Avaliacao_Poster_DemoDay.md` critério 3. Redefinir a
> régua de Mobile exige atualizar **três** documentos, não só a direction.

### A22. A prova de autoria não define o que acontece em caso de reprovação — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** o professor definiu **uma segunda tentativa**, em data marcada pelo professor,
> com prazo limite **03/12/2026 (quinta-feira)** — uma semana antes da primeira noite do evento, para que
> a lista de habilitados esteja fechada antes dele. **Reprovando na segunda
> tentativa: reprovado na disciplina, sem participar do Poster + Demo Day**, sem terceira tentativa e sem
> nota de apresentação a calcular.
>
> Acrescentado o bloco *Reprovação e segunda tentativa* em `Portfolio.md` § Prova de Autoria, com a
> ressalva na tabela de habilitação de que esta é a **única** condição com segunda chance. Propagado para
> `demoday/Avaliacao_Poster_DemoDay.md` (nova seção de pré-condição — fecha também o **M22**) e
> `demoday/guia_poster.md`.

Registro do problema original:

`Portfolio.md:47-64`

O documento define o que é verificado, quando ocorre e que a aprovação é condição para o Demo Day.
**Não define a consequência da reprovação:** há reaplicação? em que prazo? é reprovação direta na
disciplina, ou só perda da habilitação para apresentar (com a nota ficando em aberto)?

O **M11** foi marcado resolvido tendo definido *o que se verifica* — a consequência ficou de fora.

### A23. Faixa 6,0–7,0: "pode condicionar" × "é condicionada"

`documentation/diretrizes-avaliacao-professores.md:53` × `:60`, `:71-72` × `RFC:541`

- `:53` — *"Entre 6,0 e 7,0 o avaliador **pode** condicionar a validação a correções obrigatórias."*
- `:60` — *"Entre 6,0 e 7,0 a aprovação **é** condicionada a correções."*
- `:71-72` (tabela, notas 6,5 e 6,0) — *"As correções apontadas **são obrigatórias** para validação."*
- `RFC:541` — *"6,0 a 6,5 — Aprovada **com correções obrigatórias**"*

Um avaliador que leia só `:53` registra 6,5 sem exigir correção nenhuma — e, pelas outras três fontes,
essa RFC deveria cair abaixo de 6,0 e reprovar. Some-se `:54`, que autoriza *"ajustes obrigatórios"* em
**qualquer** nota, inclusive nas plenamente aprovadas, sem definir consequência para o não cumprimento.

## 🟡 MÉDIO — estrutura, terminologia e lacunas

### M15. O núcleo comum de engenharia não tem cabeçalho em duas das cinco linhas

`webapp.md` e `mobile.md` × `ia.md:15`, `iot.md:17`, `jogosdigitais.md:14`

IA, IoT e Jogos têm `### Núcleo comum de engenharia` isolando os cinco requisitos compartilhados.
Webapp e Mobile trazem **os mesmos cinco itens diluídos** na lista de obrigatórios, sem cabeçalho.

O conteúdo está lá; a estrutura não. O leitor não distingue núcleo compartilhado de requisito específico,
e a próxima alteração do núcleo tende a esquecer justamente essas duas linhas.

### M16. "Temas a evitar" e "Temas impedidos" existem em duas linhas e faltam em três

Presentes em `webapp.md:88,94` e `mobile.md:83,92`. Ausentes em IA, IoT e Jogos, embora a tabela do
GERAL traga temas 🚫 **Não Usar** aplicáveis a qualquer linha.

### M17. A sanção do critério 1 é "desclassificação"; a do critério 5 é "reprovação imediata"

`demoday/Avaliacao_Poster_DemoDay.md:49` × `:116-124`

Critério 1: *"cópias diretas sem personalização podem levar à **desclassificação**"*. Critério 5:
*"resultam em **reprovação imediata**"*. Dois termos para o quê — e apenas o critério 5 está declarado
**eliminatório**. Não está claro se copiar tutorial desclassifica de fato, nem o que "desclassificação"
significa em termos de nota.

### M18. A mesma estrutura de squad tem dois nomes

`PAC Extensionista VII.md:36` — *"**Squads de Suporte**: grupos de 3 a 5 participantes"*.
`PAC Extensionista VIII.md:17` — *"**Squads de Validação** (3 a 5 alunos)"*.

### M19. Referência aponta na direção errada

`PAC Extensionista VIII.md:57` — *"a **evidência equivalente** descrita **abaixo**"*. A Seção 3.1 está
**acima**, na linha 30. O item `:78` acerta: *"descrito na Seção 3.1"*.

### M20. As ferramentas de monitoramento divergem entre avaliação e GERAL

`Avaliacao_Poster_DemoDay.md:106` exemplifica **Logtail** e **Railway Insights**, que não constam da
tabela ✅ Preferir do GERAL (Zabbix, Prometheus, Grafana, Dynatrace, New Relic, Datadog).

### M21. `locais_publicacao.md` não cobre a linha de Jogos Digitais

Lista apenas provedores de nuvem. A direction de Jogos exige **build pública distribuída** (Itch.io,
loja, WebGL hospedado, APK) como equivalente ao ambiente produtivo — nenhum deles aparece no documento
que existe para orientar onde publicar.

### M22. Nada no documento de avaliação diz que só projetos habilitados são avaliados — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** criada a seção **🚦 Pré-condição: apenas trabalhos habilitados são avaliados** no topo
> de `demoday/Avaliacao_Poster_DemoDay.md`, antes do *Formato de Avaliação*, nomeando os dois gates
> (cinco orientações · prova de autoria com segunda tentativa) e apontando para os *Requisitos de
> Aprovação*. Fechado junto com o **A22**.

Registro do problema original:

`demoday/Avaliacao_Poster_DemoDay.md` é o documento que o professor usa no dia. Não menciona que
**cinco orientações evidenciadas** e **prova de autoria aprovada** são pré-condição para o trabalho
estar ali. O avaliador não tem como saber que um trabalho não habilitado não deveria receber nota.

## ⚪ BAIXO — texto e forma

### B15. A grafia do evento varia dentro do mesmo repositório

| Grafia | Onde |
|---|---|
| `Poster + Demo Day` (forma canônica) | 18 ocorrências |
| `DemoDay` | `Portfolio.md:65,154` · `README.md:31` · `PAC Extensionista VIII.md:60` |
| `Demoday` | `Portfolio.md:91` |

### B16. Erro de concordância no README

`README.md:17` — *"Validação do projeto em desenvolvimento **junta a** Comunidade ou parceiro externo"*
→ *"junto à Comunidade"*.

### B17. Três resíduos de formatação no PAC VII — ✅ **RESOLVIDO em 25/07/2026**

> **Resolução:** os três corrigidos. De carona, um quarto problema encontrado ao inserir a seção
> *6. Prazos*: as etapas **3, 4 e 5 estavam em `####`**, aninhadas sob a etapa 2, em vez de `###` como as
> etapas 1 e 2 — a numeração dizia que eram irmãs, a hierarquia dizia que eram filhas. As seis etapas
> agora estão no mesmo nível. Também normalizado `### 2 Organização` → `### 2. Organização`.

Registro do problema original:

- `:74` — *"NP3 (60%):Entrega Final"* — falta espaço após os dois-pontos.
- `:26` — linha termina com `\` solto (quebra de linha Markdown órfã).
- `:85` — `##  Objetivo da Etapa` com espaço duplo após o `##`.

### B18. `locais_publicacao.md` é o único documento sem H1

Começa em `## Locais para Publicar o APP`. O título fala em "APP", mas o documento serve às cinco linhas.

### B19. Vultr listado como "nível gratuito"

`demoday/locais_publicacao.md:14` — a Vultr oferece **crédito promocional**, não free tier permanente,
diferente dos outros quatro da lista.

### B20. RFC § 7 usa "Semana X/Y/Z" sem âncora de calendário

`documentation/RFC/modelo-de-RFC.md:499-503` — enquanto o restante do repositório passou a usar datas
absolutas no formato `DD/MM/AAAA (dia da semana)`, a tabela de marcos do template segue em semanas
relativas, sem ponto de partida declarado.

## 💡 Melhorias estruturais (não são inconsistências)

1. **Fonte única para o calendário.** `30/11/2026` aparece em 3 arquivos e as três datas do evento em
   outros 3. Um documento (ou seção) de calendário do semestre, referenciado pelos demais, elimina a
   classe inteira de divergência de datas — e resolve o A20 de carona.
2. **Padronizar o esqueleto das cinco directions** (núcleo comum + temas) fecha M15 e M16 de uma vez e
   torna a próxima mudança do núcleo mecânica em vez de manual.
3. **Amarrar o critério 3 aos números da linha** fecha o C9 sem criar regra nova: basta o critério citar
   a cobertura obrigatória da direction.
4. **Checklist cronológico do aluno** — um documento com os gates em ordem (2 orientações até 30/09 · 5
   orientações + prova de autoria + entrega até 30/11 · visita e avaliação dos colegas em dezembro).
   Hoje essa sequência só existe reconstruída a partir de três documentos.
5. **README deveria expor os Requisitos de Aprovação.** As seis participações obrigatórias só aparecem
   no `Portfolio.md`; quem entra pelo README não as encontra.
6. **Colisão de numeração na RFC § 5.1:** dentro dela existem `## 1. Nível 1`, `## 2. Nível 2` e
   `## 3. Nível 3`, que colidem com a numeração de topo do documento.
7. **Padronizar links em caminhos relativos** — recomendação do B1, ainda não executada.

---

## Ordem sugerida de correção

**Bloco 1 — desbloquear avaliadores e alunos** — ✅ **CONCLUÍDO em 25/07/2026**
~~C1~~ · ~~C2~~ · ~~C4~~ · ~~C5~~ · ~~C6~~ (+ ~~B13~~, feito de carona) — referências de seção renumeradas
contra o RFC atual, ficha de avaliação com nota e assinatura criada na Seção 10 do template,
três links quebrados corrigidos e verificados contra o sistema de arquivos.

**Bloco 2 — fechar as regras de nota** — ✅ **CONCLUÍDO em 25/07/2026**
~~C7~~ · ~~C8~~ · ~~A17~~ — pesos 90/10 fixados, fórmula Likert→0-10 escrita e limiar de aprovação
do RFC definido em 6,0, com faixa condicional de 6,0 a 7,0.

**Bloco 3 — decidir e propagar (discussão de colegiado)** — ✅ **CONCLUÍDO em 25/07/2026**
~~A1~~ · ~~A2~~ (o que é "banca") · ~~A3~~–~~A5~~ · ~~A7~~ · ~~A13~~ · ~~A14~~ (o que é obrigatório para
*todas* as linhas × o que é específico) · ~~A15~~ · ~~A16~~ — núcleo comum de engenharia padronizado nas
cinco linhas, exceções de Jogos Digitais nomeadas, modalidade Comunidade com evidência equivalente.

**Bloco 4 — limpeza estrutural** — ✅ **CONCLUÍDO em 25/07/2026**
~~C3~~ · ~~M1~~ (`disciplina-portfolio.md` removido) · ~~M2~~ · ~~M4~~ · ~~M5~~ · ~~M8~~ · ~~B1~~ · ~~B14~~.

**Bloco 5 — revisão de texto** — ✅ **CONCLUÍDO em 25/07/2026**
~~B2~~–~~B13~~.

**Bloco 6 — regras de participação** — ✅ **CONCLUÍDO em 25/07/2026**
~~M12~~ — cinco orientações (duas até 30/09/2026) como gate de habilitação, mais participação como
visitante e avaliação dos colegas como gate de aprovação. Seção *Requisitos de Aprovação* criada em
`Portfolio.md` e propagada para os dois documentos do Demo Day.

### Recomendação registrada e não executada

O B1 corrigiu o **nome do repositório** nos links (`-I` → atual), mas a recomendação de **padronizar
tudo em links relativos** (`./directions/...`) não foi executada — os documentos seguem usando URL
absoluta `https://github.com/.../blob/main/...`, exceto o `README.md`. Links relativos sobrevivem a
renomeação de repositório e funcionam em clones locais. Decisão pendente, sem impacto normativo.
