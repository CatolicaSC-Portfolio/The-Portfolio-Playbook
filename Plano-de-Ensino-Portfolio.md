# Plano de Ensino — Portfólio de Projeto

> **Documento de trabalho.** Rascunho para preenchimento do formulário institucional (código da
> disciplina G1441, turma T2ESOFT08NB). Substitui o plano vigente, herdado de Trabalho de Conclusão de
> Curso I — ver o diagnóstico ao final. Campos marcados com `[confirmar no PPC]` dependem de dados
> institucionais que não estão neste repositório. Fonte normativa do conteúdo:
> [Disciplina de Portfólio](Portfolio.md), [Directions](directions/portfolio-directions-GERAL.md),
> [Avaliação do Poster + Demo Day](demoday/Avaliacao_Poster_DemoDay.md) e
> [Calendário 2026/2](calendario.md). Este plano recebe conteúdo desses documentos e nunca o contrário.

---

## DISCIPLINA

**PORTFÓLIO DE PROJETO**

- **Curso:** Engenharia de Software
- **Professor(es):** Diogo Vinicius Winck
- **Ano/Semestre:** 2026/2 (202623)
- **Carga horária:** `[confirmar no PPC]` — **70h (84 h/a)**. A distribuição por unidade adiante
  (14h · 40h · 16h) foi definida pelo professor.

---

## OBJETIVO GERAL DO CURSO

> Formar um profissional ético e inovador, com conhecimento técnico e científico para atuar em pesquisa,
> gestão, desenvolvimento, aplicação e avaliação de tecnologias da informação, considerando a segurança e
> as questões socioambientais.

---

## JUSTIFICATIVA DA DISCIPLINA NO CURSO

A disciplina de Portfólio de Projeto é a etapa de execução da trajetória de projeto do curso. No PAC
Extensionista VII o acadêmico identificou um problema real, investigou o estado da arte e formalizou sua
proposta técnica em uma RFC avaliada por três professores. No Portfólio essa proposta vira produto: o
acadêmico implementa a arquitetura e as tecnologias definidas na RFC e entrega uma solução funcional,
publicada em ambiente produtivo com acesso público. Em paralelo, o PAC Extensionista VIII
verifica e valida o mesmo produto com revisão por pares e com o parceiro externo ou a comunidade.

A disciplina integra, em um único projeto individual e autoral, conhecimentos que o curso desenvolveu em
separado: requisitos, arquitetura, padrões de projeto, testes, integração e entrega contínuas,
observabilidade, documentação e gestão do próprio trabalho. A exigência não é que o software "funcione",
mas que seja construído com práticas profissionais verificáveis — histórico de commits, pipeline de
CI/CD, análise estática, monitoramento, Wiki — e que resista a revisão de código, a defeitos reportados
por colegas e a pedidos de mudança do parceiro.

A disciplina se encerra em público. No Poster + Demo Day o acadêmico demonstra o produto em
funcionamento e o defende diante de três professores e da comunidade acadêmica, comunicando decisões
técnicas a públicos diferentes. Antes disso, a prova de autoria confirma que o acadêmico domina o que
entregou. O uso de assistentes de IA não é proibido, mas não dispensa esse domínio. Com isso, a
disciplina prepara o egresso para responder, como profissional, por cada decisão e por cada linha do que
entrega.

---

## EMENTA

> Desenvolvimento de aplicações. Padrões de Projeto. Projeto Final.

---

## OBJETIVO GERAL DA DISCIPLINA

Capacitar o acadêmico a executar, de forma individual e autoral, a solução concebida na RFC do PAC
Extensionista VII, aplicando práticas profissionais de engenharia de software — padrões de projeto,
testes, integração e entrega contínuas, observabilidade e documentação — até disponibilizá-la em
ambiente produtivo e defendê-la publicamente no Poster + Demo Day.

---

## HABILIDADES DESENVOLVIDAS PELA DISCIPLINA

- **Planejamento e gestão:** decompor a RFC em backlog e em entregas incrementais (MVPs); planejar o
  semestre contra marcos fixos; gerir riscos, mudanças de escopo e o próprio tempo.
- **Construção de software:** implementar a arquitetura proposta; aplicar princípios SOLID, padrões de
  projeto e Clean Architecture; refatorar para legibilidade e desempenho.
- **Qualidade e verificação:** escrever testes automatizados com o instrumento adequado à linha de
  projeto; incorporar revisão de código e defeitos reportados por terceiros ao desenvolvimento; usar
  análise estática de código e de segurança.
- **Engenharia de entrega:** configurar pipeline de CI/CD; manter ambientes distintos de desenvolvimento
  e produção; publicar e operar a solução em nuvem, loja ou build distribuída; definir e implantar
  monitoramento ou observabilidade.
- **Documentação:** registrar arquitetura, requisitos e decisões técnicas em Wiki, de modo a viabilizar
  contribuições externas ao projeto.
- **Comunicação e defesa técnica:** justificar decisões de engenharia e trade-offs perante avaliadores;
  sintetizar o projeto em pôster técnico; demonstrar a solução a públicos técnico e não técnico.
- **Avaliação crítica e ética:** avaliar trabalhos de colegas com critérios explícitos; responder pela
  autoria do que entrega, inclusive do que foi produzido com apoio de IA.

---

## UNIDADES, CONTEÚDOS E AVALIAÇÃO

As três unidades seguem a ementa. Elas se sobrepõem no tempo — o desenvolvimento é contínuo do início
ao fim do semestre —, e a ordem indica onde está o foco de cada fase.

### Unidade I — Desenvolvimento de Aplicações: da RFC ao plano de execução

**Conteúdos.**
- 1.1 Contrato pedagógico da disciplina: requisitos de entrega, de habilitação e de aprovação
- 1.2 Retomada da RFC: problema, escopo, arquitetura proposta e critérios de aceite
- 1.3 Linhas de projeto (Web Apps, Mobile, IA, IoT, Jogos Digitais) e seus critérios obrigatórios
- 1.4 Tabela mestra de tecnologias, processos e temas
- 1.5 Decomposição da RFC em backlog e fatiamento em entregas incrementais (MVPs)
- 1.6 Planejamento do semestre contra os marcos do calendário; identificação de riscos
- 1.7 Repositório, fluxo de versionamento e Wiki iniciais
- 1.8 Articulação com o PAC Extensionista VIII: como revisões e defeitos reportados viram tarefas

**Objetivos de aprendizagem.** Compreender as regras que habilitam, aprovam e reprovam na disciplina.
Retomar criticamente a RFC e convertê-la em um plano executável. Identificar os critérios obrigatórios
da própria linha de projeto. Planejar entregas incrementais compatíveis com os marcos do semestre e com
as validações do PAC VIII. Antecipar os riscos técnicos do projeto.

**Metodologia.** Aula expositiva dialogada sobre o contrato pedagógico e as directions. Orientações
individuais, presenciais ou remotas, para retomada da RFC e validação do plano de execução. Montagem do
repositório, do backlog e da Wiki, com acompanhamento por inspeção do repositório.

**Avaliação — formativa.** Feedback nas orientações sobre o plano de execução e o backlog. Marco de
habilitação: **duas primeiras orientações evidenciadas até 30/09/2026 (quarta-feira)**, por ata enviada
por e-mail, foto ou registro equivalente. Não gera nota; sem esse marco, o aluno não se habilita ao
Poster + Demo Day.

**Cronograma.** `[confirmar no PPC]` — 14h. Encerra-se com o marco de 30/09/2026
(quarta-feira).

**Recursos.** Laboratório de informática; acesso à internet; GitHub (repositório, issues, Wiki);
ferramenta de gestão de backlog; [Directions](directions/portfolio-directions-GERAL.md).

---

### Unidade II — Padrões de Projeto e Engenharia de Software Aplicada

**Conteúdos.**
- 2.1 Princípios SOLID, padrões de projeto e Clean Architecture aplicados ao projeto
- 2.2 Desenvolvimento contínuo: commits frequentes e histórico de evolução legível
- 2.3 Testes automatizados por linha de projeto: metas, TDD e o instrumento adequado a cada tecnologia
- 2.4 Revisão de código e refatoração a partir dos *code reviews* do PAC VIII
- 2.5 Resolução de issues: defeitos reportados por colegas e melhorias pedidas pelo parceiro
- 2.6 Núcleo comum de engenharia: Wiki, CI/CD, análise estática de código e segurança, monitoramento ou
  observabilidade
- 2.7 Ambientes de desenvolvimento e produção; deploy em nuvem, loja ou build distribuída
- 2.8 Gestão de mudanças de escopo e acompanhamento das entregas incrementais
- 2.9 Jogos Digitais: playtest com público e relatório de playtest

**Objetivos de aprendizagem.** Aplicar padrões de projeto e princípios de arquitetura na solução
proposta, justificando cada escolha. Manter o desenvolvimento em ritmo contínuo e rastreável. Escrever
testes que verifiquem comportamento, e não apenas atinjam um percentual. Incorporar revisão de código e
defeitos reportados por terceiros como tarefas de desenvolvimento. Implantar e operar o núcleo comum de
engenharia. Publicar a solução em ambiente estável, sem dependência de máquina local.

**Metodologia.** Aprendizagem baseada em projeto, com desenvolvimento individual e contínuo.
Orientações individuais com revisão técnica do repositório: arquitetura, histórico de commits, testes,
pipeline e issues abertas. As revisões por Pull Request e os testes cruzados feitos pelos colegas no PAC
VIII entram no backlog como tarefas obrigatórias. Na linha de Jogos Digitais, playtest com no mínimo 10
participantes na noite oficial ou de forma independente, com evidências.

**Avaliação — formativa.** Feedback individual nas orientações e pela inspeção dos repositórios, com
atenção à evolução do histórico e ao tratamento das issues. Sem nota. Marco de habilitação no período,
**só para Jogos Digitais**: playtest com no mínimo 10 participantes — na noite oficial de
**26/10/2026 (segunda-feira)** ou de forma independente, com evidências — e relatório do playtest até
**30/10/2026 (sexta-feira)**. Ver as [Diretrizes de Playtest](documentation/games/Diretrizes-Playtest.md).

**Testes por linha de projeto.** A meta obrigatória de cobertura não é igual entre as linhas e é
conferida na prova de autoria, não pontuada na nota:

| Linha | Meta obrigatória de cobertura | TDD |
|---|---|---|
| Web Apps | 75% no backend / 25% no frontend | obrigatório |
| Mobile · IA · IoT · Jogos Digitais | nenhuma — testes com o instrumento próprio de cada linha são desejáveis | preferível |

Em Mobile, o TDD e a meta de 75% / 25% voltam a ser obrigatórios se o acadêmico escrever o próprio
backend.

**Cronograma.** `[confirmar no PPC]` — 40h. Do início do semestre ao prazo de entrega de
**30/11/2026 (segunda-feira)**.

**Recursos.** Laboratório de informática; acesso à internet; GitHub (Pull Requests, issues, Actions,
Wiki); ferramentas de análise estática e de monitoramento; provedor de nuvem, loja de apps ou
plataforma de distribuição de jogos; [direction](directions/portfolio-directions-GERAL.md) da linha.

---

### Unidade III — Projeto Final: consolidação, prova de autoria e Poster + Demo Day

**Conteúdos.**
- 3.1 Verificação final contra os requisitos de entrega e os critérios obrigatórios da linha
- 3.2 Release em ambiente produtivo público e estável até a divulgação das notas
- 3.3 Consolidação da documentação de arquitetura, requisitos e decisões técnicas
- 3.4 Prova de autoria: domínio do codebase, das decisões de engenharia e do próprio trabalho
- 3.5 Pôster técnico (A0 vertical, template oficial, QR Code de acesso à aplicação)
- 3.6 Demonstração funcional e defesa técnica no Poster + Demo Day
- 3.7 Avaliação dos trabalhos dos colegas como membro da comunidade acadêmica

**Objetivos de aprendizagem.** Consolidar o produto e sua documentação em versão de entrega. Demonstrar
domínio do próprio trabalho e justificar arquitetura, tecnologias, padrões e trade-offs. Sintetizar o
projeto em pôster técnico. Apresentar e defender a solução em funcionamento para professores e
comunidade. Avaliar o trabalho de colegas com critérios explícitos.

**Metodologia.** Orientações individuais de fechamento até completar as cinco. Prova de autoria
individual, no último encontro da disciplina. Preparação do pôster a partir do
[Guia do Pôster](demoday/guia_poster.md). Apresentação no Poster + Demo Day e participação como
visitante em uma noite distinta, avaliando os trabalhos apresentados pelo formulário oficial.

**Avaliação — habilitação.**
- **Cinco orientações evidenciadas** até **30/11/2026 (segunda-feira)**.
- **Prova de autoria aprovada** até **30/11/2026 (segunda-feira)**. Ela verifica autoria e, na linha
  de Web Apps (e no backend próprio de um projeto Mobile), a cobertura de testes. Admite **uma segunda tentativa** até **03/12/2026
  (quinta-feira)**; reprovar duas vezes é **reprovação na disciplina**, sem apresentar.
- **Todos os requisitos de entrega**, inclusive os critérios obrigatórios da linha, até **30/11/2026
  (segunda-feira)**.

**Avaliação — somativa: Poster + Demo Day.** Única nota da disciplina, de 0 a 10, com uma casa
decimal. Três professores avaliam seis critérios de peso igual em escala Likert de 1 a 5:
(1) Relevância e Complexidade, (2) Documentação, (3) Qualidade Técnica do Código, (4) Infraestrutura e
Engenharia, (5) Ética, Integridade e Autoria, (6) Apresentação no Evento. A nota de cada professor é a
média dos critérios × 2. A nota final é 90% a média dos professores e 10% a nota da comunidade
acadêmica. O critério 5 é **eliminatório**: plágio, falsificação de resultados ou uso indevido de dados
resultam em reprovação, independentemente das demais notas. Detalhes em
[Avaliação do Poster + Demo Day](demoday/Avaliacao_Poster_DemoDay.md).

**Avaliação — participação.** Visitar uma noite do evento, distinta daquela em que apresenta, com
presença registrada, e avaliar os trabalhos apresentados nela. É requisito de aprovação, não item de
nota.

**Destaque.** Os projetos que mais se destacarem em inovação, qualidade técnica e impacto são
convidados para uma Banca Técnica Especial e recebem menção de destaque. Não altera a nota.

**Cronograma.** `[confirmar no PPC]` — 16h, incluindo as noites do evento, cuja presença
registrada conta como aula regular. Poster + Demo Day: **10/12/2026 (quinta-feira)**, **15/12/2026
(terça-feira)** e **16/12/2026 (quarta-feira)**.

**Recursos.** Laboratório de informática e projetor; acesso à internet; ambiente produtivo de
hospedagem da solução; [template do pôster](demoday/TEMPLATE_POSTER_PORTFOLIO.pptx); espaço do evento;
formulário ou aplicativo oficial de avaliação.

---

## METODOLOGIA (síntese)

Aprendizagem baseada em projeto, com um projeto individual e autoral desenvolvido ao longo de todo o
semestre a partir da RFC do PAC VII. Aulas expositivas dialogadas pontuais, sobre o contrato pedagógico,
as directions e a avaliação. No mínimo cinco orientações individuais, presenciais ou remotas, com
revisão técnica do repositório. Inspeção contínua dos repositórios. Revisões de código e testes
cruzados vindos do PAC VIII. Na linha de Jogos Digitais, playtest com público. Prova de autoria
individual e apresentação pública no Poster + Demo Day.

---

## SÍNTESE DA AVALIAÇÃO

| Instrumento | Natureza | Prazo | Efeito |
|---|---|---|---|
| Feedback nas orientações e inspeção do repositório | formativa | contínuo | orienta; sem nota |
| Duas primeiras orientações evidenciadas | habilitação | 30/09/2026 (quarta-feira) | sem elas, não apresenta |
| Playtest e relatório — só Jogos Digitais | habilitação | relatório até 30/10/2026 (sexta-feira); noite oficial em 26/10/2026 (segunda-feira) ou playtest independente | sem eles, não apresenta |
| Cinco orientações evidenciadas | habilitação | 30/11/2026 (segunda-feira) | sem elas, não apresenta |
| Requisitos de entrega e critérios obrigatórios da linha | habilitação | 30/11/2026 (segunda-feira) | sem eles, trabalho não entregue |
| Prova de autoria | habilitação | 30/11/2026 (segunda-feira) · 2ª tentativa até 03/12/2026 (quinta-feira) | duas reprovações = reprovado na disciplina |
| Poster + Demo Day | **somativa — nota única** | 10/12/2026 · 15/12/2026 · 16/12/2026 | aprovação com nota ≥ **6,0** |
| Visita a uma noite e avaliação dos colegas | aprovação | durante o evento | sem ela, reprovado |

Nenhum requisito de habilitação ou de aprovação é compensado por nota. A régua Destaque / Aprovado /
Reprovado de cada linha está na respectiva [direction](directions/portfolio-directions-GERAL.md).

---

## BIBLIOGRAFIA

As duas obras do plano vigente que tratam do conteúdo da ementa foram mantidas como estavam (Freeman,
com número de chamada; Massari, livro eletrônico). As demais são sugestões e precisam ser conferidas no
acervo (edição, disponibilidade e número de chamada). Os seis títulos de metodologia científica do plano
vigente não correspondem à ementa e foram retirados.

### Básica

- SOMMERVILLE, Ian. *Engenharia de software*. 10. ed. São Paulo: Pearson Education do Brasil, 2018.
  `[conferir acervo]`
- GAMMA, Erich et al. *Padrões de projeto: soluções reutilizáveis de software orientado a objetos*.
  Porto Alegre: Bookman, 2000. `[conferir acervo]`
- MARTIN, Robert C. *Arquitetura limpa: o guia do artesão para estrutura e design de software*. Rio de
  Janeiro: Alta Books, 2019. `[conferir acervo]`

### Complementar

- FREEMAN, Eric. *Use a cabeça! Padrões e projetos*. 2. ed. rev. Rio de Janeiro: Alta Books, 2010.
  005.12 F93u 2. ed. CG
- MASSARI, Vitor L. *Agile Scrum Master no gerenciamento avançado de projetos*. Rio de Janeiro:
  Brasport, 2016. ISBN 9788574527857. Livro eletrônico.
- FOWLER, Martin. *Refatoração: aperfeiçoando o design de códigos existentes*. 2. ed. São Paulo:
  Novatec, 2020. `[conferir acervo]`
- HUMBLE, Jez; FARLEY, David. *Entrega contínua: como entregar software de forma rápida e confiável*.
  Porto Alegre: Bookman, 2014. `[conferir acervo]`
- BECK, Kent. *TDD: desenvolvimento guiado por testes*. Porto Alegre: Bookman, 2010.
  `[conferir acervo]`

---

## Diagnóstico do plano vigente (202623)

| Campo | Situação no plano vigente | Tratamento |
|---|---|---|
| Justificativa | Fala de "Trabalho de Conclusão de Curso I" e de pesquisa | Reescrita a partir de `Portfolio.md` |
| Objetivo geral da disciplina | Orienta "definição de um tema, pesquisa e desenvolvimento do TCC" | Reescrito — tema e RFC são do PAC VII |
| Habilidades | Problemas, metodologia e instrumentos de pesquisa | Reescritas a partir dos pilares de `Portfolio.md` |
| Unidades | "Aspectos metodológicos" e "Projeto de pesquisa", com ABNT e LaTeX | Reorganizadas pelos três itens da ementa |
| Avaliação | "Confecção de artigo" e "apresentação de trabalhos" | Gates de habilitação + Poster + Demo Day |
| Cronograma | 30/04, 29/05 e 04/07, datas de outro semestre | Substituído pelas datas de `calendario.md` |
| Bibliografia | Seis obras de metodologia científica | Retiradas; mantidas Freeman e Massari |
| Ementa e objetivo geral do curso | Corretos | Mantidos |

## Sugestões de revisão: como foram consideradas

As sugestões do parecer de revisão do plano foram usadas como referência, não como texto a transcrever.
Onde contradizem a regra vigente do repositório, prevaleceu o repositório.

| Sugestão do parecer | Tratamento | Motivo |
|---|---|---|
| Justificativa mais ampla | Adotada, com texto próprio | Ancorada na trajetória PAC VII → Portfólio → PAC VIII |
| Objetivo geral mais específico | Adotada, adaptada | Inclui a origem na RFC e o encerramento no Demo Day |
| Habilidades por categoria | Adaptada | Categorias próprias; a de trabalho coletivo não foi adotada — o projeto é individual |
| Unidades alinhadas à ementa, com sumário numerado | Adotada | Os títulos seguem os três itens da ementa |
| Metodologia detalhada | Adotada, adaptada | Sem apresentações parciais nem orientação coletiva, que não existem nas regras |
| Avaliação formativa explícita | Adotada | Orientações, inspeção do repositório e gates, sem nota |
| NP1 / NP2 / NP3 por unidade, questionários, tarefas | **Não adotada** | Decisão do professor: nota única no Demo Day; o acompanhamento é feito pelos gates sem nota |
| Carga horária de 70h (84 h/a) | Adotada | Pendente de confirmação no PPC |

---

## Decisões tomadas na elaboração

1. **Nota única.** O parecer pede uma nota parcial por unidade (NP1 / NP2 / NP3). Decisão do professor:
   manter a nota única no Poster + Demo Day. O acompanhamento ao longo do semestre fica a cargo dos gates
   sem nota, descritos em cada unidade como avaliação formativa e de habilitação.
2. **Distribuição da carga horária:** 14h · 40h · 16h, definida pelo professor.
3. **Cobertura de testes em Jogos Digitais:** a meta de 50% foi retirada da direction da linha, que se
   contradizia com `Portfolio.md`, o guia de avaliação e o calendário. Só Web Apps tem meta.

## Campos pendentes de confirmação

1. **Carga horária oficial** — 70h (84 h/a), a confirmar no PPC.
2. **Bibliografia** — conferir no acervo edição, disponibilidade e número de chamada das obras sugeridas.
