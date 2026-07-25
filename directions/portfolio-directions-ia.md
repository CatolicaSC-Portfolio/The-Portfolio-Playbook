# Linha de Projeto – Projetos com Inteligência Artificial (IA)

## O que é obrigatório atender
Requisitos mínimos e obrigatórios para habilitação ao Poster + Demo Day.

- Deve aplicar, de maneira fundamentada, uma ou mais abordagens de IA em um problema real no domínio do tema escolhido. As abordagens aceitas incluem, mas não se limitam a:  
  - **IA clássica híbrida com Rede Neural Artificial**: Sistemas Especialistas ou Otimização (exemplos de técnicas aceitas: GA+ANN, FIS+ANN);  
  - **Aprendizagem de Máquina (ML/DL)**: Modelos para Classificação, Regressão ou Clustering, Reconhecimento de Padrões em imagens, sons ou sinais, Visão Computacional, Detecção de Anomalias, Processamento de Linguagem Natural, Sistemas de Recomendação (para ML serão aceitos técnicas Ensembles, tais como: Baggin, Boosting, Stacking. Para DL serão aceitos técnicas FNN, MLP, CNN, RNN, GAN, etc.);  
  - **Modelos Generativos**: NLP Generativa, Transformer, RAG, Fine-tuning de modelos LLMs;  
- Deve apresentar propósito prático e funcional (ser parte integrante de uma aplicação);
- Caso a solução da proposta requeira dados, deve fazer uso de base de dados real ou sintética, desde que acompanhada de justificativas devidamente embasadas. Caso não seja necessário de dados, a decisão deve ser justificada;
- Deve contemplar o pipeline funcional de IA, incluindo etapas como extração/geração de dados, pré-processamento (método científico, matemática, estatística), modelo IA, pós-processamento (visualização, testes, validação e implantação do modelo);
- Deve considerar aspectos de responsabilidade ética, incluindo a privacidade de dados (como previsto na LGPD) e o cumprimento de normas ou legislações específicas da área de aplicação, como, por exemplo, na área da saúde;

### Núcleo comum de engenharia

Requisitos válidos para **todas as linhas de projeto**, conforme o [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md):

- **Documentação em Wiki** junto ao repositório (Wiki do GitHub ou equivalente).
- **Pipeline CI/CD** configurado e funcionando (ex.: GitHub Actions, GitLab CI).
- **Análise estática de código e segurança** (ex.: SonarQube, SonarCloud, CodeClimate).
- **Monitoramento ou observabilidade** da solução em execução.
- **Cobertura de testes automatizados: 70%** do código de aplicação e do pipeline de IA — notebooks exploratórios ficam fora da contagem.

---

## O que é desejável atender
Melhora a qualidade do projeto. Fortemente recomendado, mas não elimina se ausente.

- Possuir interface (web ou app) para interação com a IA;
- Ter modelo de arquitetura para acomodar o pipeline da solução;
- Apresentar métricas de desempenho e análise dos resultados;
- Realizar validação do modelo com técnica adequada (k-fold, holdout, etc.);
- Apresentar justificativa clara para escolha do algoritmo/modelo;
- Possuir infraestrutura de IA em nuvem (AWS, Azure, etc.).

---

## O que é um diferencial
Características que elevam o nível do projeto e podem gerar destaque e convites.

- Desenvolvimento de modelo próprio (em vez de apenas usar um pré-treinado);
- Avaliação com usuários reais ou especialistas do domínio;
- Resultados publicados em eventos, hackathons ou desafios externos;

---

## O que deve ser evitado
Más práticas que reduzem a percepção de qualidade, mesmo em projetos funcionais.

- Uso de IA sem aplicação real;
- Base de dados genérica não relacionada ao problema;
- Ausência de testes ou evidência de funcionamento;

---

## O que não pode ter
Erros graves que causam desclassificação ou reprovação direta.

- Plágio de código ou conteúdo copiado de notebooks da internet sem adaptação ou compreensão;
- Modelo com resultados aleatórios ou não replicáveis;
- Código hardcoded, low-code/no-code ou sem modularização;
- Base de dados inválida, falsa ou não autorizada;
- Utilizar dataset pronto como dados da solução;
- Violação ética: uso indevido de dados sensíveis, práticas discriminatórias, deepfakes não autorizados, etc.;

---

## Régua de Avaliação

- **Destaque** — além de todos os obrigatórios, demonstra diferencial técnico ou criativo: modelo próprio, arquitetura robusta ou validação rigorosa (cross-validation, análise de métricas), e disponibiliza a IA para testes com usuários no dia da apresentação. Concorre a menção de destaque e a convite para a **Banca Técnica Especial**.
- **Aprovado** — atende a **todos** os itens *obrigatórios*, incluindo o núcleo comum de engenharia: aplicação funcional de uma abordagem de IA a um problema real, pipeline completo (dados, pré-processamento, modelo, pós-processamento), documentação coerente e resultados replicáveis. Nota final igual ou superior a **6,0**.
- **Reprovado** — deixa de atender a qualquer item *obrigatório*, incorre em item de *“o que não pode ter”*, ou obtém nota final abaixo de **6,0**.
