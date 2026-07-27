# Linha de Projeto – Web Apps

## O que é obrigatório atender
Requisitos mínimos e obrigatórios para habilitação ao Poster + Demo Day.

- O sistema deve estar hospedado em ambiente acessível publicamente (ex.: AWS, GCP, Azure, Hostinger, servidor institucional).
- Deve conter funcionalidades completas e reais, conforme o escopo definido no RFC.
- Interface funcional, navegável e com usabilidade básica.
- Arquitetura de software definida conforme o RFC (ex.: MVC, arquitetura em camadas, client-server).  
  - Organização modular do código (componentes reutilizáveis, separação de responsabilidades).
- Código-fonte disponível em repositório com histórico de commits.
- Documentação mínima contendo:
  - requisitos funcionais;
  - casos de uso ou user stories;
  - diagrama de arquitetura - utilizando diagramas C4 ou equivalente;
  - instruções de deploy.
- O sistema deve contemplar **ao menos três fluxos de negócio completos**.
- **Cobertura de testes unitários com TDD** — 75% no backend e 25% no frontend. Esta é a **única linha** com meta de cobertura obrigatória, conferida na **prova de autoria**: não atingindo, o aluno corrige e tem uma segunda tentativa até 03/12/2026 (quinta-feira); reprovando de novo, reprova na disciplina. Ver [Prova de Autoria](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md).

### Núcleo comum de engenharia

Requisitos válidos para **todas as linhas de projeto**, conforme o [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md):

- **Documentação em Wiki** junto ao repositório (Wiki do GitHub ou equivalente).
- **Pipeline CI/CD** configurado e funcionando (ex.: GitHub Actions, GitLab CI).
- **Análise estática de código e segurança** (ex.: SonarQube, SonarCloud, CodeClimate).
- **Monitoramento ou observabilidade** da aplicação (ex.: NewRelic, Datadog, Zabbix, Prometheus, Grafana).

---

## O que é desejável atender
Fortemente recomendado para elevar a qualidade do projeto, mas não obrigatório.

- Uso de frameworks modernos (React, Vue, Angular, etc.) com boas práticas de desenvolvimento.
- Integração com APIs externas (REST, GraphQL).
- Uso de banco de dados com persistência real (SQL/NoSQL).
- Responsividade (design adaptável a diferentes tamanhos de tela).
- Aplicação de testes de integração.
- Adoção de práticas de segurança (ex.: HTTPS, validação de entradas).
- Estratégias de cache (ex.: Nginx, Redis, Memcached).
- Uso de containerização (ex.: Docker, Podman).

---

## O que é um diferencial
Aspectos que elevam o nível do projeto e podem gerar destaque e convites.

- Autenticação robusta (OAuth2, login social com Google ou Facebook, autenticação multifator).
- Dashboards com visualizações de dados (gráficos, relatórios dinâmicos).
- Implementação de camada de segurança (ex.: JWT, proteção contra XSS/CSRF).
- Suporte multilíngue.
- Design System ou biblioteca de componentes personalizados.
- Testes de usabilidade com usuários reais e feedback documentado.
- Uso de domínio próprio (ex.: www.nomeprojeto.com).
- Processamento assíncrono com mensageria (ex.: Kafka, RabbitMQ).
- Infraestrutura como código (IaC) — ex.: Terraform.

---

## O que deve ser evitado
Más práticas que reduzem a qualidade e a legibilidade do projeto.

- Estilo visual inconsistente ou não responsivo.
- Interface genérica ou desorganizada.
- Ausência de feedback ao usuário (ex.: carregamento, erros, confirmações).
- Uso de bibliotecas, templates ou temas prontos sem personalização.
- Falta de modularidade (ex.: todo o código concentrado em um único arquivo).
- Vibecoding (código improvisado, sem planejamento).
- Uso de ferramentas de documentação como Notion ou Obsidian (não aceitas para entrega oficial).
- Hospedagem em plataformas otimizadas apenas para frontend (ex.: Vercel, Netlify, Firebase, Render). Desde **2026-02** estão 🚫 **Não Usar**, com ou sem backend próprio.
- Plataformas que automatizam totalmente backend, banco de dados e APIs sem gestão da arquitetura (no-code disfarçado de desenvolvimento).
- Serviços de cloud que ocultam infraestrutura e automação de deploy (com integração direta via GitHub e SSL automático) **sem domínio técnico sobre o ambiente.**

---

## O que não pode ter
Erros graves que causam **reprovação direta**, independentemente das demais notas.

- Projeto não acessível (link quebrado, servidor fora do ar).
- Código copiado ou plagiado (repositórios, tutoriais, templates).
- Interface inoperante (botões, menus ou links não funcionam).
- Violação de segurança básica (dados sensíveis expostos, permissões abertas, etc.).
- Ausência de documentação mínima.
- Deploy manual via SSH ou FTP.
- Uso de processo em cascata (sem práticas iterativas ou integração contínua).
- Plataformas no-code (ex.: Bubble.io, Webflow, Carrd, Thunkable, Bravo Studio, HubSpot CMS).
- Banco de dados em disco local (ex.: H2, SQLite).

---

## Temas a evitar
- Soluções que utilizam IA apenas via prompt, sem integração efetiva ou arquitetura própria.
- Sistemas genéricos de gestão de listas (livros, filmes, músicas, etc.), similares a Goodreads.

---

## Temas impedidos
- Sistema de cardápio online / QR Code.
- Sistema de controle de estoque.
- Sistema de tele-entrega.
- Sistema de gestão financeira (com ou sem IA).

---

## Régua de Avaliação

- **Destaque** — além de todos os obrigatórios, contempla os itens *desejáveis* e ao menos **um** item de *“é um diferencial”*, sem incorrer em nada de *“o que deve ser evitado”*. Concorre a menção de destaque e a convite para a **Banca Técnica Especial**.
- **Aprovado** — atende a **todos** os itens *obrigatórios*, incluindo o núcleo comum de engenharia, os três fluxos de negócio completos e a cobertura de testes (75% backend / 25% frontend). Nota final igual ou superior a **6,0**.
- **Reprovado** — deixa de atender a qualquer item *obrigatório*, incorre em item de *“o que não pode ter”*, ou obtém nota final abaixo de **6,0**.
