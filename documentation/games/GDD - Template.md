# Game Design Document (GDD)

# [Nome do Jogo]

**Aluno:** Nome Sobrenome  
**E-mail:** aluno@catolica.edu  

**Status do Projeto:**  
Pesquisa / Prototipagem / Produção / Beta / Finalizado

**Versão do Documento:** v0.1  
**Última atualização:** DD/MM/AAAA

---

# 1. Visão Geral

## Elevator Pitch

Descreva o jogo em **2–3 frases**. "Equivalente a explicar sobre o jogo em 30s a 1m"

Exemplo:

> Um jogo de plataforma 2D onde o jogador controla um robô tentando escapar de uma fábrica automatizada resolvendo puzzles baseados em física.

---

## Gênero

Exemplo:

- Plataforma
- Puzzle
- Roguelike
- Estratégia

---

## Público-Alvo

Exemplo:

Jogadores casuais entre 16 e 35 anos que gostam de jogos rápidos e desafiadores.

---

## Plataformas

- PC
- Web
- Mobile

---

# 2. Acesso ao Projeto

| Item | Link |
|-----|-----|
| Build jogável | Itch.io / WebGL / Download |
| Repositório | GitHub |
| Vídeo gameplay (opcional) | YouTube |
| Instruções de execução | Requisitos técnicos |

---

# 3. Pesquisa e Referências

## Jogos de Referência

Liste **2–5 jogos que inspiraram o projeto**.

para cada jogo descreva  brevemente o jogo, os aspectos que inspiram. Adicione imagens para ilustrar.

---

## Análise das Referências

Explique brevemente:

- o que esses jogos fazem bem
- quais ideias inspiraram seu projeto

---

# 4. Hipóteses de Design

Liste hipóteses que serão testadas durante o desenvolvimento.

| Hipótese | Como será testada |
|-----|-----|
| jogadores gostam de progressão rápida | playtest com fases curtas |
| combate simples melhora acessibilidade | protótipo com 1 botão de ataque |

## Pilares do jogo

- 3 a 5 no máximo

---

# 5. Gameplay

## Core Loop

Descreva o ciclo principal do jogo.

Exemplo:

Explorar → enfrentar inimigos → coletar recursos → melhorar personagem → continuar explorando

## Loops Secundários

---

## Mecânicas Principais

| Mecânica | Descrição |
|-----|-----|
| Movimento | como o jogador se desloca |
| Combate | como o jogador ataca |
| Interação | como interage com objetos |


## Camera

- Tipo de câmera

---

## Sistemas

**Vitória**

Condição para vencer.

**Derrota**

Condição para perder.

**Progressão**

Sistema de níveis, pontos ou upgrades.

---

# 6. Escopo do Projeto

Defina claramente **o que será implementado**.

## O jogo inclui

- X fases
- X tipos de inimigos
- X mecânicas principais

## O jogo não inclui

- multiplayer online
- sistema complexo de crafting
- geração procedural avançada

---

# 7. Prototipagem

Descreva os protótipos realizados durante o desenvolvimento.

| Protótipo | Objetivo | Resultado |
|-----|-----|-----|
| movimento básico | validar controle | aprovado |
| combate | testar ritmo | precisa ajustes |

---

# 8. Interface (UI/UX)

## HUD

Elementos visíveis durante o jogo.

*Adicione imagens/prototipos/mockups de tela*

Exemplo:

- barra de vida
- pontuação
- timer

---

## Menus

*Adicione imagens/prototipos/mockups de tela*

- menu principal
- pause
- game over
- configurações

## Flow de menus

- diagrama

## Controles

- diagrama e disposição dos inputs e o que fazem


---

# 9. Direção Visual

## Direção de Arte

*Adicione imagens/prototipos/ mood board*

Exemplo:

- pixel art
- low poly
- cartoon

---

## Referências Visuais

Links ou imagens que inspiram o estilo do jogo.

---

# 10. Áudio

Liste os áudios do jogo em tabela: tipo, onde é usado, se tem loop e descrição.

| Áudio | Onde usa | Loop | Descrição |
|-----|-----|-----|-----|
| tema principal | menu | sim | melodia calma, piano |
| impacto | acerto no inimigo | não | curto, grave |

Tipos comuns: música de fundo, efeitos sonoros, narração.

---

# 11. Animação

Liste todas as animações em tabela: qual é, onde é usada, se tem loop e descrição.

| Animação | Onde usa | Loop | Descrição |
|-----|-----|-----|-----|
| corrida | movimento lateral | sim | 8 frames |
| dano | ao levar hit | não | flash + recuo |

---

# 12. Arquitetura de Software

Descreva a estrutura geral do código.

Exemplo:

- GameManager central
- sistema de eventos
- scripts separados por responsabilidade

---

## Tecnologias Utilizadas

| Categoria | Ferramenta |
|-----|-----|
| Engine | Unity / Godot / Unreal |
| Linguagem | C# / GDScript / C++ |
| Versionamento | Git + GitHub |
| Assets | Asset Store / OpenGameArt |

---

# 13. Testes e Playtests

## Playtests

| Data | Participantes | Principais problemas |
|-----|-----|-----|
| DD/MM/AAAA | 5 pessoas | controles confusos |
| DD/MM/AAAA | 10 pessoas | dificuldade elevada |

---

## Melhorias Implementadas

Problema → solução aplicada.

Exemplo:

Jogadores não entendiam o objetivo inicial → tutorial adicionado.

---
# 14. Cronograma

detalhe os principais milestones do projeto.


# 15. Riscos do Projeto

| Risco | Impacto | Mitigação |
|-----|-----|-----|
| IA muito complexa | atraso no projeto | simplificar comportamento |
| performance baixa | experiência ruim | otimizar ou reduzir inimigos |

---

# 16. Limitações Conhecidas

Liste funcionalidades planejadas mas não implementadas.

Exemplo:

- multiplayer online
- sistema de save em nuvem
- novas fases

---

# 17. Decisões Importantes

Registro de mudanças relevantes durante o projeto.

| Data | Decisão | Motivo |
|-----|-----|-----|
| DD/MM/AAAA | remover sistema de crafting | escopo muito grande |
| DD/MM/AAAA | adicionar dash | melhorar mobilidade |

---

# 18. Créditos

Liste assets externos utilizados.

| Recurso | Fonte | Licença |
|-----|-----|-----|
| sprites | OpenGameArt | CC0 |
| música | compositor X | CC-BY |

---

# 19. Reflexão Final

Explique brevemente:

- principais desafios
- aprendizados técnicos
- o que faria diferente

1–3 parágrafos são suficientes.
