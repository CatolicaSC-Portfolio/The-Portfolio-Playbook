# Avaliação – Poster + Demo Day

A avaliação final será realizada durante o Poster + Demo Day, considerando as notas atribuídas pelos professores e pela comunidade acadêmica.

A avaliação busca reconhecer o aprendizado, a aplicação prática de competências e a capacidade de apresentar soluções de forma crítica e integrada.
Mais do que mensurar desempenho, o processo visa promover reflexão, autonomia técnica e evolução contínua dos estudantes.

## 🚦 Pré-condição: apenas trabalhos habilitados são avaliados

Antes de avaliar, o trabalho já passou pelos gates de habilitação da disciplina:

- **Cinco orientações evidenciadas** — duas até 30/09/2026 (quarta-feira), as cinco até 30/11/2026 (segunda-feira).
- **Aprovação na prova de autoria**, que confere autoria e — **só na linha de Web Apps** — a meta de cobertura de testes.

A prova de autoria admite **uma segunda tentativa**, até **03/12/2026 (quinta-feira)**; reprovar duas vezes reprova na disciplina. A lista de habilitados está fechada antes da primeira noite do evento. Trabalho não habilitado **não apresenta** e não recebe nota — logo, tudo que chega à sua mesa já passou por esses gates. Regra completa em [Requisitos de Aprovação](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md).

---

## 🔑 Formato de Avaliação
- Cada trabalho será avaliado por:
  - **Três professores**, com formulário Likert e comentários qualitativos — **peso 90%**.
  - Uma **quarta nota**, resultado da média de todas as notas recebidas da comunidade durante o Demo Day — **peso 10%**.
- A **média ponderada** dessas notas resultará em uma **única nota final** (0 a 10).
- A avaliação será registrada em **formulário ou aplicativo**, utilizando **escala Likert** para cada critério e espaço para comentários qualitativos.
- Professores receberão antecipadamente:
  - Lista de trabalhos.
  - Links para repositórios e documentações.

---

## 🎯 Escala Likert (descritores de referência)

| Nível | Descrição | Significado prático |
|:------|:-----------|:--------------------|
| **1** | Insuficiente | Não atende aos critérios mínimos; demonstra falhas conceituais ou técnicas. |
| **2** | Básico | Atende parcialmente; há lacunas significativas na execução ou fundamentação. |
| **3** | Adequado | Cumpre o esperado de forma satisfatória, com coerência e funcionalidade. |
| **4** | Avançado | Supera expectativas em alguns aspectos, evidenciando domínio técnico e clareza conceitual. |
| **5** | Excelência | Demonstra maturidade técnica e conceitual, originalidade e integração plena entre teoria e prática. |

---

## ✅ Critérios de Avaliação

### 1. Relevância e Complexidade

Relevância, escopo claro e originalidade: projeto resolve problema real, tem funcionalidades bem definidas e evita copiar tutoriais, garantindo propósito próprio e aplicação prática.

*Detalhamento:*

* **Problema real** – o projeto aborda uma necessidade concreta e significativa.  
  *Exemplos:* gestão de filas hospitalares, automação de processos contábeis, monitoramento ambiental.  
  *Implicação:* temas genéricos ou sem aplicação prática reduzem a nota.

* **Escopo e funcionalidades** – bem definidos, com metas alcançáveis e coerentes.  
  *Exemplo:* sistema de reservas com login, listagem e cancelamento, evitando excesso de funcionalidades não implementadas.

* **Originalidade e propósito** – evita replicar tutoriais ou modelos prontos.  
  *Exemplo:* projeto inspirado em app conhecido, mas com proposta diferente ou contexto local.  
  *Implicação:* cópia sem personalização **reduz a nota deste critério**. Se for plágio — código, design ou texto copiados — aplica-se o **critério 5**, que é eliminatório e reprova de imediato.

---

### 2. Documentação

Documentação completa, organizada e rastreável: inclui motivação, requisitos, arquitetura, instruções, registro claro de decisões técnicas e materiais coerentes, legíveis e fáceis de entender.

*Detalhamento:*

* **Repositório completo** – inclui motivação, requisitos, modelagem, arquitetura e instruções de uso.  
  *Exemplo:* README com diagrama de arquitetura, instruções de execução e histórico de decisões.

* **Registro de decisões** – documentação de escolhas técnicas e mudanças.  
  *Exemplo:* uso de RFCs, ADRs ou issues no GitHub.  
  *Implicação:* ausência de registro indica falta de método de engenharia.

* **Clareza e organização** – textos, diagramas e instruções de fácil compreensão.  
  *Exemplo:* diagramas legíveis e coerentes com o código-fonte.

---

### 3. Qualidade Técnica do Código

Código bem estruturado, modular e legível, com boas práticas, testes automatizados e histórico de commits claro que evidencie evolução contínua e responsabilidade técnica.

*Detalhamento:*

* **Estrutura e modularização** – código organizado por camadas e responsabilidades.  
  *Exemplo:* controller, service, repository, separação de frontend e backend.

* **Boas práticas** – uso consistente de padrões da linguagem e estilo de código.  
  *Exemplo:* linters, convenções de nomes, tratamento de erros.

* **Testes automatizados** – qualidade e pertinência dos testes unitários e/ou de integração.  
  *Exemplo:* Jest, PyTest, JUnit, Postman/Newman.  
  *Implicação:* testes rasos, que só perseguem percentual sem exercitar regra de negócio, reduzem a nota.  
  > **Não avalie cobertura por percentual.** Só a linha de **Web Apps** tem meta obrigatória (75% backend / 25% frontend), e ela é **gate** conferido na prova de autoria — quem não atinge corrige, tem uma segunda tentativa e, reprovando de novo, não chega ao evento. Em **Mobile, IA e IoT não existe meta de cobertura**: testes unitários não se aplicam bem a essas tecnologias, e o esperado ali é teste instrumentado, de integração, validação de modelo ou das rotinas críticas de firmware. Neste item pontue **o que os testes valem** — se exercitam regra de negócio de fato — não quanto medem. Ver [Prova de Autoria](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md).

* **Histórico de commits** – progresso contínuo e colaborativo.  
  *Exemplo:* commits frequentes e mensagens descritivas.

---

### 4. Infraestrutura e Engenharia

Engenharia madura: versionamento consistente, CI/CD funcional, monitoramento básico, práticas de segurança aplicadas e deploy automatizado com uso de ferramentas DevOps modernas.

*Detalhamento:*

* **Versionamento** – controle de branches e issues.  
  *Exemplos:* GitHub, GitLab, Bitbucket.

* **CI/CD (Integração e Entrega Contínua)** – pipeline automatizado de build, testes ou deploy.  
  *Exemplos:* GitHub Actions, GitLab CI, Jenkins, Codemagic, Bitrise, Unity Cloud Build.  
  *Implicação:* ausência de automação indica baixa maturidade de engenharia.  
  *Atenção:* Vercel e Netlify **não contam como pipeline de CI/CD** — são plataformas de hospedagem com deploy automático, e desde **2026-02** estão marcadas 🚫 **Não Usar** no [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md). Ver a ressalva do critério 6.

* **Monitoramento e observabilidade** – logs e métricas básicas configuradas.  
  *Exemplos:* Zabbix, Prometheus, Grafana, Dynatrace, New Relic, Datadog — as ferramentas ✅ Preferir do [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md).

* **Segurança** – uso de variáveis de ambiente, HTTPS, autenticação segura.  
  *Exemplos:* JWT, OAuth2, proteção contra XSS/CSRF.

* **Práticas DevOps** – deploy documentado, uso de containers ou scripts automatizados.  
  *Exemplos:* Docker, Docker Compose, AWS, GCP, Azure.

---

### 5. Ética, Integridade e Autoria

Autoria real, sem plágio, com uso ético e responsável de dados; violações como cópias, falsificações ou mau uso implicam reprovação imediata.

*Detalhamento:*

* **Autoria genuína** – o projeto é resultado do trabalho original do acadêmico, sem cópias de código, design ou texto.  
* **Uso ético de dados** – respeita princípios de privacidade, LGPD e boas práticas de pesquisa.  
  *Implicação:* plágio, falsificação de resultados ou uso indevido de dados resultam em reprovação imediata.  

---

### 6. Apresentação no Evento (Poster + Demo Day)

Apresentação clara, demonstração funcional, domínio técnico nas respostas e pôster autoexplicativo com identidade consistente; falhas visuais ou operacionais reduzem impacto.

*Detalhamento:*

* **Clareza e narrativa** – explicação direta do problema, solução e resultados.  
  *Exemplo:* storytelling com foco no impacto da solução.

* **Demonstração funcional** – sistema acessível e operante em ambiente produtivo.  
  *Exemplos:* aplicação hospedada em nuvem (AWS, GCP, Azure, Magalu Cloud), servidor institucional, app publicado em loja ou build jogável em plataforma pública.  
  *Atenção:* Vercel, Netlify e Render **não são aceitas como ambiente produtivo** — desde **2026-02** estão 🚫 **Não Usar** no [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md), em **todas as linhas**, com ou sem backend próprio. Em Jogos Digitais a build pública vai para Itch.io, loja ou APK.

* **Domínio técnico** – o autor demonstra segurança ao responder perguntas.  
  *Exemplo:* justificar escolha de arquitetura, linguagem, bibliotecas e métricas.

* **Pôster técnico** – conteúdo autoexplicativo, com QR Code funcional e identidade visual coerente.  
  *Implicação:* pôster incompleto ou ilegível reduz percepção de profissionalismo.

---

## ⭐ Participação da Comunidade Acadêmica

- A comunidade acadêmica também avaliará os projetos, atribuindo notas de **originalidade** e **clareza de apresentação**.  
- A nota da comunidade será incorporada à média final com **peso de 10%**, valorizando o engajamento e a comunicação científica.
- **Os alunos da disciplina integram essa comunidade e avaliar é obrigatório para eles.** Cada aluno deve participar como **visitante de uma noite** do evento — distinta daquela em que apresenta — e avaliar os trabalhos apresentados nessa noite pelo formulário oficial. É requisito de **aprovação na disciplina**, não item de nota: ver [Requisitos de Aprovação](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md). A comprovação da presença é o registro do evento.

---

## 📏 Escala Final

- **Nota Final:** média ponderada das avaliações (0 a 10) — **90% professores** (média dos três avaliadores) e **10% comunidade**.  
- A avaliação privilegia **aprendizado, consistência, originalidade e ética profissional** como pilares de excelência.

### Como a Likert vira nota

A conversão da escala Likert (1 a 5) para a nota (0 a 10) é feita **multiplicando por 2**.

**Passo a passo:**

1. **Nota de cada professor** = média dos 6 critérios (Likert 1–5) **× 2**.
2. **Nota dos professores** = média das notas dos três avaliadores.
3. **Nota da comunidade** = média de todas as notas recebidas do público, convertida pela mesma regra (**× 2**).
4. **Nota Final** = (nota dos professores **× 0,9**) + (nota da comunidade **× 0,1**), arredondada em **uma casa decimal**.

**Exemplo:**

| Etapa | Cálculo | Resultado |
|:--|:--|:--|
| Professor 1 — critérios 4, 3, 4, 3, 5, 4 | média 3,83 × 2 | 7,7 |
| Professor 2 | — | 8,0 |
| Professor 3 | — | 7,3 |
| Nota dos professores | (7,7 + 8,0 + 7,3) ÷ 3 | 7,7 |
| Nota da comunidade | Likert médio 4,2 × 2 | 8,4 |
| **Nota Final** | (7,7 × 0,9) + (8,4 × 0,1) | **7,8** |

**Observações:**

- A nota mínima possível por esta fórmula é **2,0** (Likert 1 em todos os critérios). Notas abaixo disso só ocorrem por **reprovação direta**.
- O critério **5 — Ética, Integridade e Autoria** é **eliminatório**: plágio, falsificação de resultados ou uso indevido de dados resultam em **reprovação imediata**, independentemente das demais notas. Não entra na média nesses casos.
- Os **6 critérios têm peso igual** entre si dentro da nota de cada professor.
