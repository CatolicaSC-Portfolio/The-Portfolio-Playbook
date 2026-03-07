# Guia de Preenchimento e Boas Práticas

## Game Design Document (GDD)

Este documento orienta o preenchimento do **Game Design Document (GDD)**
utilizado nos projetos de games do Portfólio Acadêmico.

O GDD descreve o conceito, design, arquitetura e desenvolvimento do
jogo.\\
Ele funciona como um **registro evolutivo do projeto** e deve ser
atualizado ao longo de todo o desenvolvimento.

O template oficial do GDD está disponível no arquivo:

`GDD - Template.md`

Este guia explica **como preencher cada seção do template** e apresenta
**boas práticas para a documentação do projeto**.

---- 

# Objetivo do GDD

O Game Design Document possui três objetivos principais:

1.  **Planejamento do jogo**\\
	Organizar as ideias principais antes da implementação.

2.  **Registro do desenvolvimento**\\
	Documentar decisões tomadas durante o projeto.

3.  **Documentação final**\\
	Permitir que outras pessoas compreendam o projeto.

O documento deve evoluir ao longo do desenvolvimento.

---- 

# Estrutura do Documento

O template do GDD está organizado nas seguintes seções principais:

1.  Informações gerais\\
2.  Acesso ao projeto\\
3.  Visão geral do jogo\\
4.  Pesquisa e referências\\
5.  Gameplay\\
6.  Escopo do projeto\\
7.  Prototipagem\\
8.  Interface (UI/UX)\\
9.  Direção visual\\
10. Áudio\\
11. Arquitetura de software\\
12. Testes e playtests\\
13. Riscos do projeto\\
14. Limitações conhecidas\\
15. Créditos\\
16. Reflexão final

Cada seção possui um objetivo específico.

---- 

# Informações Gerais

Esta seção identifica o projeto.

Inclui:

-   nome do jogo
-   autor
-   contato
-   status do projeto
-   versão do documento
-   data da última atualização

### Boas práticas

Atualize a **versão do documento** sempre que fizer mudanças relevantes.

Exemplo:

	v0.1 — versão inicial
	v0.3 — atualização de gameplay
	v1.0 — versão final

---- 

# Acesso ao Projeto

Esta seção permite que avaliadores e outras pessoas acessem o projeto.

Inclua:

-   build jogável
-   repositório de código
-   vídeo de gameplay (opcional)
-   instruções de execução

### Recomendações

O avaliador deve conseguir:

-   acessar o repositório
-   executar o jogo
-   entender rapidamente como o projeto funciona

Evite exigir configurações complexas para rodar o jogo.

---- 

# Visão Geral do Jogo

Apresenta o conceito geral do projeto.

Inclui:

-   elevator pitch
-   gênero
-   público-alvo
-   plataformas

### Elevator Pitch

Explique o jogo em **2 ou 3 frases**.

Um bom pitch responde rapidamente:

-   que tipo de jogo é
-   o que o jogador faz
-   qual o diferencial do jogo

---- 

# Pesquisa e Referências

Liste jogos que inspiraram o projeto.

Não se trata apenas de citar jogos conhecidos.\\
Explique **quais ideias foram aproveitadas**.

Exemplo:

  Jogo      Inspiração
---- 
  Celeste   controle preciso do personagem
  Hades     progressão entre partidas

### Boas práticas

Evite apenas listar jogos sem análise.\\
Mostre **como eles influenciaram o design**.

---- 

# Gameplay

Esta é uma das seções mais importantes do documento.

Ela descreve **como o jogo funciona**.

Inclui:

-   core loop
-   mecânicas principais
-   regras de vitória e derrota
-   progressão

### Core Loop

	Explorar → enfrentar inimigos → coletar recursos → melhorar personagem

Todo o jogo gira em torno desse ciclo.

---- 

# Escopo do Projeto

Esta seção define claramente **o que será implementado**.

Projetos acadêmicos devem ter **escopo realista**.

### O jogo inclui

Funcionalidades que fazem parte do projeto.

### O jogo não inclui

Funcionalidades fora do escopo.

Isso ajuda a evitar crescimento descontrolado do projeto.

---- 

# Prototipagem

Game development envolve **experimentação**.

Nesta seção registre protótipos realizados durante o projeto.

Exemplo:

  Protótipo              Objetivo
---- 
  sistema de movimento   validar controle do personagem
  combate                testar ritmo do jogo

Nem todo protótipo precisa virar parte do jogo final.

---- 

# Interface (UI/UX)

Descreve como o jogador interage com o jogo.

Inclui:

-   HUD
-   menus
-   elementos de interface

Exemplo de HUD:

-   barra de vida
-   pontuação
-   timer

---- 

# Direção Visual

Descreve o estilo artístico do jogo.

Exemplos:

-   pixel art
-   cartoon
-   low poly

Também podem ser incluídas **referências visuais**.

---- 

# Áudio

Descreve os elementos sonoros do jogo.

Exemplos:

-   música de fundo
-   efeitos sonoros
-   narração

---- 

# Arquitetura de Software

Descreve como o jogo foi estruturado tecnicamente.

Inclua:

-   principais sistemas
-   organização do código
-   tecnologias utilizadas

Exemplo:

  Categoria       Ferramenta
---- 
  Engine          Unity
  Linguagem       C\#
  Versionamento   Git

### Recomendações

A arquitetura deve seguir princípios básicos de \*\*engenharia de
software\*\*:

-   modularidade
-   separação de responsabilidades
-   organização clara do código

---- 

# Testes e Playtests

Descreva testes realizados com jogadores.

Inclua:

-   número de participantes
-   problemas identificados
-   melhorias implementadas

Playtests ajudam a melhorar:

-   dificuldade
-   clareza das mecânicas
-   experiência do jogador

---- 

# Riscos do Projeto

Identifique possíveis problemas que podem afetar o desenvolvimento.

  Risco                     Impacto
---- 
  mecânica muito complexa   atraso no desenvolvimento
  baixa performance         experiência ruim

Pensar em riscos ajuda no planejamento.

---- 

# Limitações Conhecidas

Liste funcionalidades planejadas que **não foram implementadas**.

Exemplo:

-   multiplayer online
-   mais fases
-   novos inimigos

---- 

# Créditos

Liste todos os recursos externos utilizados.

  Recurso   Fonte          Licença
---- 
  sprites   OpenGameArt    CC0
  música    compositor X   CC-BY

Sempre respeite as licenças dos assets utilizados.

---- 

# Reflexão Final

Apresente uma breve reflexão sobre o projeto.

Sugestões:

-   principais desafios encontrados
-   aprendizados técnicos
-   o que poderia ser melhorado

---- 

# Recomendações Gerais

### Mantenha o documento atualizado

O GDD deve evoluir durante o projeto.

### Seja claro e objetivo

Prefira textos simples e diretos.

### Use elementos visuais

Sempre que possível inclua:

-   diagramas
-   imagens
-   fluxos de gameplay
-   screenshots

### Documente decisões importantes

Explique **por que decisões foram tomadas**.

### Evite escopo excessivo

Projetos acadêmicos devem priorizar:

-   um conceito claro
-   mecânicas bem implementadas
-   código organizado

Um jogo pequeno e bem feito é melhor que um jogo grande incompleto.
