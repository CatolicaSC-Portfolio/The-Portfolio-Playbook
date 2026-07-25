# Linha de Projeto – Aplicações Mobile

## O que é obrigatório atender
Requisitos mínimos e obrigatórios para habilitação ao Poster + Demo Day.

- O aplicativo deve estar disponível em ambiente produtivo, acessível para instalação e testes (ex.: APK instalável, publicado no Google Play, TestFlight ou hospedado em plataforma de testes como Firebase App Distribution).  
- Deve conter **funcionalidades reais e completas**, alinhadas ao escopo apresentado no RFC.  
- Deve adotar uma **arquitetura mobile compatível** (ex.: MVC, MVVM, Clean Architecture).  
- Código-fonte disponível em **repositório versionado**, com histórico de commits e boa organização de branches.  
- Interface **funcional e navegável**, testável em dispositivo real, com **QR Code no pôster** para acesso rápido à instalação.  
- Documentação mínima contendo:  
  - requisitos funcionais;  
  - casos de uso ou user stories;  
  - estrutura de navegação da aplicação;  
  - diagrama de arquitetura;  
  - instruções de deploy ou instalação.  
- Deve contemplar **ao menos três fluxos de uso completos**, que demonstrem o valor e a coerência do produto.
- Cobertura de testes unitários com TDD:
  - 75% no backend;
  - 25% no frontend.
- Aplicação de **ferramentas de análise estática e qualidade de código** (ex.: SonarQube, SonarCloud, CodeClimate).  
- Uso de **monitoramento e analytics** para acompanhamento de métricas (ex.: Firebase Analytics, App Center, Datadog).  
- Pipeline de **integração e entrega contínua (CI/CD)** (ex.: GitHub Actions, Codemagic, Bitrise).  
- **Documentação em Wiki** junto ao repositório (Wiki do GitHub ou equivalente).  

---

## O que é desejável atender
Fortemente recomendado para elevar a qualidade e robustez técnica do projeto, mas não obrigatório.

- Publicação em loja oficial (Google Play / App Store).  
- Integração com serviços externos (ex.: APIs REST, mapas, notificações push).  
- Aplicação de **testes instrumentados** (execução em dispositivo ou emulador).  
- **Responsividade e adaptação** a diferentes tamanhos de tela e dispositivos.  
- Implementação de **boas práticas de UX/UI** (ex.: Material Design, coerência visual, acessibilidade).  
- Persistência de dados local no dispositivo (ex.: SQLite, RealmDB, DataStore).  
- Aplicação de testes de integração.

> **Sobre persistência local:** o veto a banco em disco (H2, SQLite) do [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md) vale para o **banco de produção do backend**. Persistência local no dispositivo — cache, modo offline, preferências — é prática esperada em mobile e não incorre nesse veto.

  
---

## O que é um diferencial
Aspectos que demonstram maturidade técnica, refinamento de produto e potencial de destaque.

- Autenticação robusta (login social, OAuth2, biometria, autenticação multifator).  
- Sistema de métricas de uso e comportamento de usuários integrado (analytics, telemetria).  
- Interface multilíngue e suporte a internacionalização.  
- Arquitetura modular ou baseada em micro frontends (apps complexos e escaláveis).  
- Testes com usuários reais, prototipagem validada e feedback documentado.  
- Design System próprio ou biblioteca de componentes reutilizáveis.  
- Uso de **Infraestrutura como Código (IaC)** ou automação de deploy mobile (ex.: Fastlane, Terraform).  
- Integração com mensageria e notificações assíncronas (ex.: Firebase Cloud Messaging, RabbitMQ, Kafka).  

---

## O que deve ser evitado
Más práticas que reduzem a qualidade técnica, a experiência do usuário e a credibilidade do projeto.

- Aplicativos com apenas **telas estáticas** (mockups ou navegação simulada).  
- Falta de testes básicos que causem falhas críticas (crashes, travamentos).  
- Interface desorganizada, inconsistente ou mal adaptada a diferentes resoluções.  
- Funcionalidades genéricas sem propósito claro (ex.: lista de tarefas sem contexto de aplicação).  
- Ausência de feedback ao usuário em ações importantes (carregamentos, erros, confirmações).  
- Dependência excessiva de templates prontos, sem personalização ou autoria.  

---

## O que não pode ter
Erros graves que causam desclassificação ou reprovação direta.

- Plágio de aplicativos existentes sem modificações significativas.  
- Reutilização de templates prontos sem personalização ou compreensão técnica.  
- Código não modularizado (ex.: toda a lógica concentrada em um único arquivo).  
- Aplicações que não executam ou não apresentam funcionalidades ativas.  
- Violação de diretrizes da plataforma (ex.: uso indevido de permissões, coleta de dados sem consentimento, falta de política de privacidade).  
- Deploy ou distribuição sem controle de versão e rastreabilidade.  
- Aplicações que dependem exclusivamente de **plataformas no-code ou low-code**.  

---

## Temas a evitar
- Aplicativos que apenas replicam funcionalidades genéricas (ex.: lista de tarefas, agenda, controle de hábitos).  
- Aplicativos que usam **IA via prompt** sem integração real ou arquitetura própria.  
- Aplicativos de catálogo simples (ex.: listagem de produtos, serviços ou pessoas sem interação ou lógica de negócio).  
- Aplicativos que simulam redes sociais sem proposta inovadora.  
- Aplicativos de “portfólio pessoal” ou “currículo digital” sem recursos interativos ou contexto técnico.  

---

## Temas impedidos
- Aplicativos de cardápio online / QR Code.  
- Aplicativos de controle de estoque.  
- Aplicativos de delivery / tele-entrega.  
- Aplicativos financeiros genéricos (com ou sem IA).  
- Aplicativos de lista de compras ou tarefas sem diferencial técnico.  

---

## Régua de Avaliação

- **Destaque** — além de todos os obrigatórios, contempla os itens *desejáveis* e ao menos **um** item de *“é um diferencial”*, sem incorrer em nada de *“o que deve ser evitado”*. Concorre a menção de destaque e a convite para a **Banca Técnica Especial**.
- **Aprovado** — atende a **todos** os itens *obrigatórios*, incluindo o núcleo comum de engenharia, os três fluxos de uso completos e a cobertura de testes (75% backend / 25% frontend). Nota final igual ou superior a **6,0**.
- **Reprovado** — deixa de atender a qualquer item *obrigatório*, incorre em item de *“o que não pode ter”*, ou obtém nota final abaixo de **6,0**.
