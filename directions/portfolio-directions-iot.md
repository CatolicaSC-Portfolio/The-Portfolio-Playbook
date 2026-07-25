# Linha de Projeto – Projetos IoT (Internet das Coisas)

## O que é obrigatório atender
Requisitos mínimos e obrigatórios para habilitação ao Poster + Demo Day.

- Além dos descritivos exigidos no RFC, é obrigatório apresentar especificações do escopo do projeto contendo:
  - Requisitos da aplicação IoT, que podem ser representados por **Diagrama Hierárquico de Requisitos (SySML)** e **Diagrama de Arquitetura** (C4 Model ou modelo em camadas contendo: camada de sensores/atuadores, camada de rede, camada de processamento de dados e camada de aplicação).  
  - Tais diagramas devem ser descritos e fundamentados.
- Implementação dos requisitos em consonância com a arquitetura aplicada ao domínio do problema abordado.
- Código-fonte no repositório do projeto, assim como os artefatos de especificação.
- Não restringir a implementação embarcada: é necessário incluir a **internet** como meio de comunicação.
- Mesmo que simplificada, é fundamental a **interação via web/mobile** (camada de aplicação) como parte da aplicação IoT, seja:
  - Interação direta (ex.: manipular configuração de dispositivo);
  - Interação indireta (ex.: consumo de dados oriundos da aplicação IoT).  
- A **camada de aplicação** deve estar hospedada em ambiente acessível publicamente e estável, não dependente de máquina pessoal.

### Núcleo comum de engenharia

Requisitos válidos para **todas as linhas de projeto**, conforme o [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md):

- **Documentação em Wiki** junto ao repositório (Wiki do GitHub ou equivalente).
- **Pipeline CI/CD** configurado e funcionando para a camada de aplicação (ex.: GitHub Actions).
- **Análise estática de código e segurança** (ex.: SonarQube, SonarCloud, CodeClimate).
- **Monitoramento ou observabilidade** da aplicação e da telemetria dos dispositivos.
- **Cobertura de testes automatizados: 60%** da camada de aplicação e de processamento de dados. No firmware, testes de unidade das **rotinas críticas** (leitura de sensores, protocolo de comunicação, tratamento de falha).

---

## O que é desejável atender
Melhora a qualidade do projeto. Fortemente recomendado, mas não elimina se ausente.

- Especificação esquemática de hardware, portas (lógica/digital), conectividade, componentes e restrições (**Diagramas de Blocos e Blocos Internos, SySML**).
- Escolha de protocolos de comunicação aderentes ao escopo do projeto.  
  - Por exemplo, ao invés de utilizar o protocolo HTTP como padrão, identificar outro que melhor satisfaça os requisitos da aplicação.

---

## O que é um diferencial
Características que elevam o nível do projeto e podem gerar destaque e convites.

- Camada de Aplicação contendo a utilização da aplicação IoT via aplicação Web ou Mobile.
- Utilização de dados oriundos da aplicação IoT em uma camada adicional contendo análise de dados e dashboards ou algum modelo de aprendizagem de máquina (predição/classificação).
- Camada de segurança com a implementação de ao menos uma prática de cibersegurança (conforme demanda do escopo do projeto).
- Integração com sistema externo à aplicação IoT.

---

## O que deve ser evitado
Más práticas que reduzem a percepção de qualidade, mesmo em projetos funcionais.

- Plataformas IoT com camadas prontas para utilização.
- Representar/simular comportamentos via utilização de LEDs, quando da falta de componentes.

---

## O que não pode ter
Erros graves que causam desclassificação ou reprovação direta.

- Apenas a simulação dos requisitos em detrimento da implementação.
- Aplicações IoT com escopo simplista, por exemplo: acender uma lâmpada, ligar um ar-condicionado, entre outros dessa natureza.
- Utilizar escopo de projetos prontos.
- Apenas a implementação embarcada.

---

## Régua de Avaliação

- **Destaque** — atende a todos os itens *obrigatórios* e *desejáveis*, mais ao menos **um** item de *“é um diferencial”*, e **não** incorre em nenhum item de *“o que deve ser evitado”*. Concorre a menção de destaque e a convite para a **Banca Técnica Especial**.
- **Aprovado** — atende a **todos** os itens *obrigatórios*, incluindo o núcleo comum de engenharia. Nota final igual ou superior a **6,0**.
- **Reprovado** — deixa de atender a qualquer item *obrigatório*, incorre em item de *“o que não pode ter”*, ou obtém nota final abaixo de **6,0**.
