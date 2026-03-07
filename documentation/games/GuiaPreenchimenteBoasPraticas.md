# Guia de Preenchimento e Boas Práticas

## Game Design Document (GDD)

Este documento orienta o preenchimento do **Game Design Document (GDD)** utilizado nos projetos de games do Portfólio Acadêmico.

O template oficial do documento está disponível em:

```
documentation/games/GDD - Template.md
```

Este guia possui dois objetivos:

1. Explicar **como preencher cada seção do template**
2. Apresentar **boas práticas de documentação para projetos de jogos**

O GDD deve ser tratado como um **documento vivo**, que evolui ao longo do desenvolvimento do projeto.

---

# Como utilizar este guia

O template define **a estrutura do documento**.

Este guia explica:

* o **objetivo de cada seção**
* **o que deve ser descrito**
* **boas práticas de documentação**

Nem todas as seções precisam estar completas no início do projeto.
Algumas partes serão refinadas conforme o desenvolvimento avança.

Sempre que possível, **inclua elementos visuais**, como:

* imagens
* screenshots
* diagramas
* wireframes
* fluxos de gameplay
* capturas do protótipo

Esses elementos tornam o documento mais claro e mais fácil de compreender.

---

# Informações Gerais do Projeto

Esta seção identifica o projeto.

Normalmente inclui:

* nome do jogo
* autor(es)
* e-mail de contato
* status do projeto
* versão do documento

## Boas práticas

Atualize o número da versão quando mudanças relevantes forem feitas.

Exemplo:

```
v0.1 – versão inicial do conceito
v0.3 – atualização de gameplay
v1.0 – versão final
```

---

# Informações de Acesso

Esta seção permite que outras pessoas acessem o projeto.

Normalmente inclui:

* build jogável
* repositório do projeto
* instruções de execução
* vídeo de gameplay (opcional)

## Recomendações

O avaliador deve conseguir:

* acessar o código
* executar o jogo
* entender rapidamente como testar o projeto

Sempre que possível, inclua:

* **prints do jogo em execução**
* **GIFs curtos demonstrando gameplay**

---

# Conceito e Visão

Esta seção apresenta a ideia central do jogo.

Normalmente inclui:

* elevator pitch
* público-alvo
* plataformas
* referências

## Elevator Pitch

Explique o jogo em **2 ou 3 frases**.

Um bom pitch responde rapidamente:

* que tipo de jogo é
* o que o jogador faz
* qual o diferencial do jogo

Se possível, inclua também:

* **imagem conceitual**
* **arte de referência**
* **mockup inicial do jogo**

---

# Público-Alvo e Plataforma

Descreva:

* quem são os jogadores
* onde o jogo será executado

Exemplo:

Público-alvo:

* jogadores casuais
* idade entre 16 e 35 anos

Plataformas possíveis:

* PC
* Web
* Mobile

Se aplicável, inclua **referências visuais de jogos voltados para o mesmo público**.

---

# Referências

Liste jogos que inspiraram o projeto.

Explique brevemente:

* o que cada jogo faz bem
* quais ideias influenciaram o seu projeto

Exemplo:

| Jogo          | Inspiração                     |
| ------------- | ------------------------------ |
| Celeste       | controle preciso do personagem |
| Hollow Knight | exploração do mapa             |

## Boas práticas

Evite apenas listar jogos.

Inclua:

* **imagens ou screenshots desses jogos**
* **elementos específicos que inspiraram seu design**

---

# Gameplay

Esta é uma das partes mais importantes do documento.

Ela descreve **como o jogo funciona**.

Normalmente inclui:

* core loop
* mecânicas principais
* regras
* sistemas

Sempre que possível, complemente a descrição com:

* **diagramas de gameplay**
* **prints do protótipo**
* **fluxogramas do jogo**

---

# Core Loop

O core loop representa o ciclo principal do jogo.

Exemplo:

```
Explorar → enfrentar inimigos → coletar recursos → melhorar personagem
```

Sempre que possível:

* apresente o core loop também como **diagrama visual**
* inclua **exemplos visuais de cada etapa**

---

# Mecânicas Principais

Liste as ações principais disponíveis para o jogador.

Exemplo:

| Mecânica  | Descrição                  |
| --------- | -------------------------- |
| Movimento | movimentação do personagem |
| Combate   | sistema de ataque          |
| Interação | interação com objetos      |

Inclua sempre que possível:

* **prints das mecânicas em funcionamento**
* **GIFs curtos do gameplay**

---

# Regras e Sistemas

Descreva as regras básicas do jogo.

Inclua:

### Condições de vitória

Como o jogador vence.

### Condições de derrota

Como o jogador perde.

### Progressão

Como o jogo evolui ao longo da partida.

Exemplos:

* fases
* níveis
* upgrades
* pontos

Se possível, inclua **diagramas ou esquemas do sistema de progressão**.

---

# Narrativa e Contexto

Se o jogo possuir narrativa, descreva:

* história básica
* personagens
* ambientação

Recomenda-se incluir:

* **arte conceitual**
* **referências visuais do mundo do jogo**
* **sketches ou storyboard**

---

# Documentação Visual

Sempre que possível inclua:

* fluxogramas
* wireframes
* storyboards
* diagramas de gameplay
* mapas de nível
* layout das fases

Essa documentação ajuda a explicar o design do jogo.

---

# Direção de Arte

Descreva o estilo visual do jogo.

Exemplos:

* pixel art
* cartoon
* low poly
* realista

Inclua sempre que possível:

* **mood boards**
* **referências visuais**
* **paletas de cores**
* **exemplos de assets**

---

# Design de Áudio

Descreva os elementos sonoros do jogo.

Exemplos:

* música de fundo
* efeitos sonoros
* narração

Se possível inclua:

* **referências de trilha sonora**
* **exemplos de estilo sonoro**

---

# Experiência do Jogador (Game Feel)

Descreva como o jogo transmite feedback ao jogador.

Isso pode incluir:

* animações
* partículas
* efeitos sonoros
* vibração

Inclua sempre que possível:

* **GIFs ou vídeos demonstrando o feedback do jogo**

---

# Interface (UI/UX)

Descreva a interface do jogo.

Inclua:

* HUD
* menus
* elementos visuais durante o gameplay

Exemplo de HUD:

* barra de vida
* pontuação
* minimapa

Inclua sempre que possível:

* **wireframes da interface**
* **prints das telas**
* **mockups de layout**

---

# Implementação Técnica

Esta seção descreve a estrutura técnica do projeto.

Inclua:

* arquitetura do sistema
* principais componentes
* tecnologias utilizadas

Exemplo:

| Categoria     | Ferramenta |
| ------------- | ---------- |
| Engine        | Unity      |
| Linguagem     | C#         |
| Versionamento | Git        |

Se possível inclua:

* **diagramas de arquitetura**
* **diagramas de componentes**
* **fluxos de sistema**

---

# Engenharia de Software e Qualidade

Explique como o projeto aborda aspectos de qualidade.

Exemplos:

* controle de versão
* pipeline de build
* deploy
* testes

Inclua sempre que possível:

* **diagramas do pipeline**
* **prints do processo de build**

---

# Testes e Playtests

Descreva testes realizados com jogadores.

Inclua:

* número de participantes
* principais problemas encontrados
* melhorias realizadas

Sempre que possível inclua:

* **prints ou vídeos de sessões de playtest**
* **gráficos simples de resultados**

---

# Limitações Conhecidas

Liste funcionalidades planejadas que **não foram implementadas**.

Exemplo:

* multiplayer online
* mais fases
* novos inimigos

---

# Créditos

Liste todos os recursos externos utilizados.

Exemplo:

| Recurso | Fonte        | Licença |
| ------- | ------------ | ------- |
| sprites | OpenGameArt  | CC0     |
| música  | compositor X | CC-BY   |

---

# Reflexão e Aprendizados

Apresente uma reflexão sobre o projeto.

Sugestões:

* principais desafios encontrados
* aprendizados técnicos
* o que poderia ser melhorado

Se possível, inclua **prints comparando versões iniciais e finais do jogo**.

---

# Recomendações Gerais

## Mantenha o documento atualizado

O GDD deve evoluir durante o desenvolvimento.

Evite deixar toda a documentação para o final.

---

## Use elementos visuais sempre que possível

Inclua:

* imagens
* diagramas
* wireframes
* prints
* GIFs
* mapas de nível

Jogos são sistemas visuais; imagens ajudam a comunicar o design.

---

## Documente decisões importantes

Explique **por que decisões foram tomadas**.

Isso ajuda a compreender a evolução do projeto.

---

## Controle o escopo

Projetos acadêmicos devem priorizar:

* um conceito claro
* mecânicas bem implementadas
* código organizado

Um jogo pequeno e bem feito é melhor que um jogo grande incompleto.

