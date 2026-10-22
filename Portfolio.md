
# 8º Semestre — Disciplina de Portfólio

No último semestre, o estudante avança da etapa de planejamento para a **consolidação e entrega final** do seu projeto.  
O foco é a **execução, documentação e apresentação pública** no evento **Poster + Demo Day** — a banca avaliadora da disciplina, em formato de apresentação aberta ao público.

## Objetivos
- Consolidar o projeto desenvolvido, garantindo qualidade técnica, inovação e responsabilidade profissional.  
- Apresentar publicamente um produto funcional em ambiente produtivo.

## Requisitos de Entrega
Para habilitar-se à apresentação final, o aluno e o projeto devem cumprir:
- **Participação em cinco orientações**, presenciais ou remotas, sendo **ao menos duas até 30/09/2026 (quarta-feira)** e as demais até **30/11/2026 (segunda-feira)**. Evidenciar cada uma é obrigação do aluno (e-mail com ata, foto ou registro equivalente), com entrega das evidências ao professor da disciplina. **Sem as cinco orientações evidenciadas — incluindo as duas do marco de setembro — o aluno não se habilita ao Poster + Demo Day**, independentemente do estado do produto.
- **Participação como visitante em uma noite do Poster + Demo Day**, além da noite em que apresenta, com avaliação ativa dos trabalhos dos colegas. Requisito de **aprovação**, detalhado em *Requisitos de Aprovação*.
- Repositório público no GitHub (com histórico de commits). **Exceção:** projetos da linha de **Jogos Digitais** podem manter repositório privado, desde que com acesso autorizado aos avaliadores.  
- Poster digital (PDF) com QR Code de acesso à aplicação.  
- Link funcional da aplicação, jogo, app, IA ou solução IoT.  
- Documentação de arquitetura, requisitos e decisões técnicas.  
- Cumprimento dos critérios obrigatórios da linha de projeto escolhida.
- Há outros requisitos em [Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md).
- Deve estar disponível em ambiente produtivo, hospedado na nuvem, com acesso público e estável (sem depender de notebook pessoal ou ambiente local) até a divulgação final das notas da disciplina. **Em Jogos Digitais**, o equivalente é a build pública e distribuída (Itch.io, loja, WebGL hospedado ou APK) — ver a [direction da linha](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-jogosdigitais.md).
  
## Pilares

### 1. Execução 

- **Implementação da RFC:** O aluno deve seguir  a arquitetura e as tecnologias definidas no semestre anterior.
- **Desenvolvimento Contínuo:** A disciplina exige ritmo. O aluno deve realizar *commits* frequentes, mantendo um histórico de evolução claro no GitHub. Devidamente revistos por pares.
- **Entregas Modulares:** O desenvolvimento é fatiado em entregas funcionais (MVPs) que servem de insumo para as validações da disciplina de PAC.
- **Documentação:** No github e que viabilize contribuições externas ao projeto.

### 2. Engenharia de Software Aplicada

Não basta "funcionar"; o código precisa ser profissional.
- **Qualidade de Código:** Aplicação de boas práticas (SOLID, Design Patterns, Clean Architecture).
- **Refatoração:** O aluno deve ter a capacidade de reescrever trechos de código para otimizar performance ou legibilidade, especialmente após receber os *Code Reviews* vindos da disciplina de PAC.
- **Resolução de Issues:** *Bugs* reportados pelos colegas (na validação do PAC) ou melhorias solicitadas pelo parceiro externo tornam-se tarefas obrigatórias de desenvolvimento aqui.

### 3. DevOps e Infraestrutura

- **CI/CD:** Configuração de *pipelines* de integração e entrega contínua.
- **Ambientes:** Manutenção de ambientes distintos (Desenvolvimento e Produção/Staging) para garantir que o parceiro externo teste uma versão estável.
- **Deploy:** O software deve estar acessível (na nuvem, na loja de apps ou em dispositivo físico), não apenas rodando em *localhost*.
- **Estratégias de Observabilidade:**  definição clara sobre como o produto será monitorado.
  


## Prova de Autoria

A **prova de autoria** é o **último encontro da disciplina**. Nele o professor questiona cada aluno sobre o próprio trabalho — o objetivo é confirmar que o projeto é de autoria genuína.

**O que é verificado:**

- **Conhecimento do codebase** — o aluno sabe onde as coisas estão, o que cada parte faz e por que está escrita daquele jeito.
- **Decisões de engenharia** — o aluno justifica arquitetura, escolha de tecnologias, padrões aplicados e trade-offs assumidos.
- **Domínio do trabalho** — o aluno explica o que construiu sem depender de anotações ou de terceiros.
- **Cobertura de testes — apenas na linha de Web Apps** (e no backend próprio de um projeto Mobile): é aqui que se confere a meta obrigatória de **75% no backend e 25% no frontend**. Nas linhas de **Mobile, IA, IoT e Jogos Digitais não há meta de cobertura**, porque testes unitários não se aplicam bem a essas tecnologias — o que se espera nelas está em *O que é desejável atender* da respectiva [direction](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md).

**Regras:**

- É **individual** e ocorre até **30/11/2026 (segunda-feira)**, junto com o prazo de entrega.
- **Aprovação na prova de autoria é condição para habilitar-se ao Poster + Demo Day.** Sem ela, o trabalho não é considerado entregue.
- Não avalia a qualidade do produto — isso é papel do Demo Day. Avalia se o trabalho é seu.
- O uso de assistentes de IA no desenvolvimento não é proibido, mas **não dispensa o domínio do resultado**: o aluno responde por cada decisão e por cada linha do que entregou.

**Reprovação e segunda tentativa:**

- Quem reprova — **por qualquer um dos itens verificados, inclusive a cobertura de testes** — tem direito a **uma segunda tentativa**, em data definida pelo professor, obrigatoriamente **até 03/12/2026 (quinta-feira)**. O prazo é anterior à primeira noite do Poster + Demo Day para que a lista de habilitados esteja fechada antes do evento.
- Reprovado por cobertura insuficiente, o aluno deve **corrigir** — escrever os testes que faltam — e voltar na segunda tentativa.
- **Reprovando na segunda tentativa, o aluno está reprovado na disciplina e não participa do Poster + Demo Day.** Não há terceira tentativa e não há nota de apresentação a ser calculada.
- Não há terceira oportunidade porque a habilitação precisa estar resolvida antes do evento — sem aprovação na prova de autoria não há trabalho entregue a apresentar.

> Autoria é o critério 5 do [Guia de Avaliação](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/Avaliacao_Poster_DemoDay.md) e é **eliminatório**: plágio ou falsificação resultam em reprovação imediata, independentemente das demais notas.

---

## Poster + Demo Day

### Apresentação
O evento é o ápice do Portfólio, reunindo estudantes, professores e comunidade acadêmica.  
Os alunos apresentam:

- Um **pôster técnico** (formato A0, orientação vertical, fonte mínima 20 pt, cores de alto contraste) contendo:  
  - Logomarca da Católica SC.  
  - Título, autor e e-mail.  
  - Contexto, problema e solução proposta.  
  - Arquitetura e decisões técnicas.  
  - Referências.  
  - QR Code para acesso à aplicação.  
  - Cabeçalho, rodapé e cores conforme o [template oficial](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/TEMPLATE_POSTER_PORTFOLIO.pptx).

  A lista completa e o checklist estão no [Guia do Pôster](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/guia_poster.md).

- Uma **demonstração funcional** do sistema em ambiente produtivo.

### Avaliação
- Cada projeto será avaliado por
   - **Três professores**, com formulário Likert e comentários qualitativos - peso: 90%
   - Uma **quarta nota** será o resultado da média de todas as notas recebidas da comunidade durante o Poster + Demo Day — peso: 10%
- A **nota final (0–10)** é a média ponderada das notas recebidas
- comunidade acadêmica poderá atribuir **menções especiais** (como “Trabalho Escolhido pela Comunidade”).

### Datas e Prazos

> Fonte única das datas: [**Calendário 2026/2**](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/calendario.md), que traz também o checklist do aluno em ordem cronológica.

**Entrega dos trabalhos:** o prazo limite é **30/11/2026 (segunda-feira)**. Até essa data o trabalho deve estar entregue e ter sido aprovado na **prova de autoria**.

O **Poster + Demo Day** — a banca avaliadora da disciplina — será realizado nos seguintes dias:

| Data | Dia da semana |
|------|---------------|
| 10/12/2026 | Quinta-feira |
| 15/12/2026 | Terça-feira |
| 16/12/2026 | Quarta-feira |

- O evento **abre 30 minutos antes** do horário de início, para que os professores possam conversar com os alunos com tranquilidade.
- Os **professores de Joinville** devem reservar essas datas para participação na avaliação.
- Haverá **registro de presença** dos alunos que participarem, para que essas horas sejam contabilizadas como aula regular. Esse registro é também a comprovação do requisito de participação como visitante (ver *Requisitos de Aprovação*).

---

## Requisitos de Aprovação

A aprovação na disciplina depende de **três blocos de condições**, em momentos diferentes. Nenhum deles é compensado por nota.

São **seis participações obrigatórias** no total: **cinco orientações** mais **uma participação como visitante** no Poster + Demo Day.

### 1. Habilitação para apresentar

| Condição | Prazo |
|---|---|
| **Duas primeiras orientações** evidenciadas | **30/09/2026 (quarta-feira)** |
| **Cinco orientações** evidenciadas (total) | **30/11/2026 (segunda-feira)** |
| **Prova de autoria** aprovada | **30/11/2026 (segunda-feira)** — segunda tentativa, se necessária, até **03/12/2026 (quinta-feira)** |
| Todos os **Requisitos de Entrega**, incluindo os critérios obrigatórios da linha de projeto | **30/11/2026 (segunda-feira)** |

Descumprida qualquer linha, o trabalho não é considerado entregue e o aluno não apresenta no Poster + Demo Day. A prova de autoria é a única condição com **segunda tentativa**; reprovar nela duas vezes é **reprovação na disciplina**, sem participação no evento.

### 2. Participação no evento — durante as noites do Poster + Demo Day

Apresentar o próprio trabalho não basta. O aluno também deve:

- **Participar como visitante de uma noite** do evento, distinta daquela em que apresenta. A comprovação é o **registro de presença**. É a sexta das seis participações obrigatórias.
- **Avaliar ativamente os trabalhos dos colegas** na noite em que atua como visitante, na condição de membro da comunidade acadêmica, pelo formulário ou aplicativo oficial. É essa participação que forma a **nota da comunidade (peso 10%)** de cada projeto — quem não avalia não sustenta o critério que a própria turma recebe.

O aluno que não cumprir as duas condições **não é aprovado na disciplina**, independentemente da nota obtida na própria apresentação.

### 3. Nota

Cumpridos os blocos 1 e 2, a aprovação exige **nota final igual ou superior a 6,0** — ver a *Régua de Avaliação* da [linha de projeto](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md). O critério **5 — Ética, Integridade e Autoria** é **eliminatório**: reprova independentemente das demais notas.

---

## Trabalhos em Destaque

Os projetos que mais se destacarem em **inovação**, **qualidade técnica** e **impacto** serão convidados para uma **Banca Técnica Especial**. Esses trabalhos receberão **menção de destaque**.

---


## 🔗 Referências e Guias

- [Guia de Avaliação do Demo Day](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/Avaliacao_Poster_DemoDay.md).
- [Guia para Poster](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/guia_poster.md).
- [Locais para publicação](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/locais_publicacao.md).
