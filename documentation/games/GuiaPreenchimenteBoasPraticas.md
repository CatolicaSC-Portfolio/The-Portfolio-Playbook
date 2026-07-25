# Guia de Preenchimento e Boas Práticas

## Game Design Document (GDD)

Este documento orienta o preenchimento do **Game Design Document (GDD)** utilizado nos projetos de games do Portfólio.

O template oficial está em [`documentation/games/GDD - Template.md`](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/documentation/games/GDD%20-%20Template.md).

> **A estrutura é a do template.** Este guia segue exatamente a mesma numeração e os mesmos títulos de seção. Se houver divergência entre os dois documentos, **vale o template**.

O GDD deve ser tratado como um **documento vivo**, que evolui ao longo do desenvolvimento.

---

## Como utilizar este guia

O template define **a estrutura**. Este guia explica, para cada seção:

* o **objetivo** dela
* **o que descrever**
* **boas práticas**

Nem todas as seções precisam estar completas no início. Algumas só fazem sentido depois das primeiras iterações.

Sempre que possível, **inclua elementos visuais** — imagens, screenshots, diagramas, wireframes, fluxos de gameplay, capturas do protótipo. Jogos são sistemas visuais; imagem comunica design melhor que texto.

**Níveis de exigência:** o GDD **mínimo** (visão geral, core loop, mecânicas, tecnologias) é *obrigatório* na linha de Jogos Digitais. O **GDD completo** — todas as seções preenchidas e mantidas atualizadas — é *desejável* e conta para Destaque. Ver [direction da linha](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-jogosdigitais.md).

---

## Cabeçalho — Identificação

Antes da Seção 1, o template pede nome do jogo, aluno, e-mail, status do projeto, versão e última atualização.

**Boas práticas**

Atualize o número da versão quando houver mudança relevante:

```
v0.1 – versão inicial do conceito
v0.3 – atualização de gameplay
v1.0 – versão final
```

Datas seguem o padrão do projeto: `DD/MM/AAAA`.

---

## 1. Visão Geral

**Objetivo:** dar ao leitor, em menos de um minuto, a compreensão do que é o jogo.

### Elevator Pitch

Explique o jogo em **2 ou 3 frases**. Um bom pitch responde:

* que tipo de jogo é
* o que o jogador faz
* qual o diferencial

Inclua, se possível, **imagem conceitual**, **arte de referência** ou **mockup inicial**.

### Gênero, Público-Alvo e Plataformas

Descreva quem são os jogadores e onde o jogo roda.

Exemplo:

* Público-alvo: jogadores casuais, entre 16 e 35 anos
* Plataformas: PC, Web, Mobile

Se aplicável, inclua **referências visuais de jogos voltados ao mesmo público**.

### Narrativa e ambientação (opcional)

Se o jogo tiver narrativa, descreva aqui história básica, personagens e ambientação — com arte conceitual, referências do mundo do jogo ou storyboard. Jogos sem narrativa podem pular.

---

## 2. Acesso ao Projeto

**Objetivo:** permitir que o avaliador acesse, execute e teste o jogo sem depender de você.

Preencha a tabela do template com build jogável, repositório, vídeo de gameplay (opcional) e instruções de execução.

**Recomendações**

O avaliador deve conseguir **acessar o código**, **executar o jogo** e **entender como testar** em poucos minutos.

Inclua **prints do jogo em execução** e **GIFs curtos** demonstrando gameplay.

> Lembre-se: em Jogos Digitais, "ambiente produtivo" significa **build pública e distribuída** (Itch.io, loja, WebGL hospedado ou APK). Build que só roda na sua máquina não é aceita.

---

## 3. Pesquisa e Referências

**Objetivo:** mostrar que o projeto está situado em relação ao que já existe.

Liste **2 a 5 jogos** que inspiraram o projeto. Para cada um, descreva brevemente o jogo e os aspectos que inspiraram.

Exemplo:

| Jogo          | Inspiração                     |
| ------------- | ------------------------------ |
| Celeste       | controle preciso do personagem |
| Hollow Knight | exploração do mapa             |

Na **Análise das Referências**, explique o que esses jogos fazem bem e quais ideias influenciaram seu design.

**Boas práticas**

Evite apenas listar. Inclua **screenshots dos jogos citados** e aponte **o elemento específico** que inspirou — "o dash do Celeste", não "Celeste".

---

## 4. Hipóteses de Design

**Objetivo:** transformar suposições em algo testável.

Toda decisão de design carrega uma aposta sobre o comportamento do jogador. Escreva essas apostas e como pretende verificá-las.

| Hipótese | Como será testada |
|---|---|
| jogadores gostam de progressão rápida | playtest com fases curtas |
| combate simples melhora acessibilidade | protótipo com 1 botão de ataque |

Volte a esta seção depois dos playtests (Seção 13) e registre se a hipótese se confirmou.

### Pilares do jogo

**3 a 5 no máximo.** São as diretrizes que resolvem discussões de escopo — quando uma ideia nova aparecer, ela deve reforçar um pilar ou ser cortada.

Exemplo: *"movimento é sempre fluido"*, *"o jogador nunca perde progresso sem entender por quê"*.

---

## 5. Gameplay

**Objetivo:** descrever como o jogo funciona. É a seção mais importante do documento.

### Core Loop

O ciclo principal, repetido pelo jogador:

```
Explorar → enfrentar inimigos → coletar recursos → melhorar personagem
```

Apresente também como **diagrama visual** e, se possível, com exemplos visuais de cada etapa.

### Loops Secundários

Ciclos de apoio ao principal — coleta opcional, missões laterais, crafting.

### Mecânicas Principais

As ações disponíveis ao jogador:

| Mecânica  | Descrição                  |
| --------- | -------------------------- |
| Movimento | movimentação do personagem |
| Combate   | sistema de ataque          |
| Interação | interação com objetos      |

Inclua **prints ou GIFs das mecânicas funcionando**.

### Camera

Tipo de câmera e por que ela foi escolhida (top-down, side-scroller, terceira pessoa, fixa). A câmera define o que o jogador consegue antecipar.

### Sistemas

**Vitória** — como o jogador vence.
**Derrota** — como o jogador perde.
**Progressão** — como o jogo evolui: fases, níveis, upgrades, pontos.

Inclua **diagrama do sistema de progressão** quando ele tiver mais de duas camadas.

---

## 6. Escopo do Projeto

**Objetivo:** declarar o tamanho do jogo antes de construí-lo.

Preencha as duas listas do template:

* **O jogo inclui** — número de fases, tipos de inimigos, mecânicas principais.
* **O jogo não inclui** — o que ficou explicitamente de fora.

A segunda lista é a mais importante. Escopo controlado é critério de avaliação: **um jogo pequeno e bem feito vale mais que um jogo grande incompleto.**

---

## 7. Prototipagem

**Objetivo:** registrar o que foi testado antes de virar produção.

| Protótipo | Objetivo | Resultado |
|---|---|---|
| movimento básico | validar controle | aprovado |
| combate | testar ritmo | precisa ajustes |

Inclua GIFs dos protótipos, mesmo dos que foram descartados — protótipo abandonado é evidência de método, não de fracasso.

---

## 8. Interface (UI/UX)

**Objetivo:** mostrar como o jogador lê o estado do jogo e navega por ele.

### HUD

Elementos visíveis durante o jogo — barra de vida, pontuação, timer, minimapa. Inclua **prints ou mockups de tela**.

### Menus

Menu principal, pause, game over, configurações. Inclua **mockups de layout**.

### Flow de menus

Diagrama mostrando a navegação entre telas.

### Controles

Diagrama com a disposição dos inputs e o que cada um faz — teclado, gamepad e/ou toque.

---

## 9. Direção Visual

**Objetivo:** definir a identidade visual antes de produzir arte em volume.

### Direção de Arte

Estilo adotado: pixel art, low poly, cartoon, realista. Inclua **mood board**, **paleta de cores** e **exemplos de assets**.

### Referências Visuais

Links ou imagens que inspiram o estilo.

---

## 10. Áudio

**Objetivo:** tratar som como sistema, não como enfeite.

Preencha a tabela com tipo de áudio, onde é usado, se tem loop e descrição:

| Áudio | Onde usa | Loop | Descrição |
|---|---|---|---|
| tema principal | menu | sim | melodia calma, piano |
| impacto | acerto no inimigo | não | curto, grave |

Inclua **referências de trilha** e exemplos do estilo sonoro pretendido.

---

## 11. Animação

**Objetivo:** listar todas as animações e onde são usadas.

| Animação | Onde usa | Loop | Descrição |
|---|---|---|---|
| corrida | movimento lateral | sim | 8 frames |
| dano | ao levar hit | não | flash + recuo |

### Game feel

É aqui que mora a sensação do jogo: animações, partículas, screen shake, vibração, resposta sonora. Inclua **GIFs ou vídeos demonstrando o feedback** — game feel não se descreve bem em texto.

---

## 12. Arquitetura de Software

**Objetivo:** mostrar que existe engenharia por trás do jogo.

Descreva a estrutura geral do código: GameManager central, sistema de eventos, scripts separados por responsabilidade. Inclua **diagrama de arquitetura ou de componentes**.

### Tecnologias Utilizadas

| Categoria | Ferramenta |
|---|---|
| Engine | Unity / Godot / Unreal |
| Linguagem | C# / GDScript / C++ |
| Versionamento | Git + GitHub |
| Assets | Asset Store / OpenGameArt |

### Núcleo comum de engenharia

A linha de Jogos também está sujeita aos requisitos obrigatórios de todas as linhas. Documente aqui:

* **Wiki** do repositório
* **Pipeline CI/CD** com build automatizado
* **Análise estática de código**
* **Monitoramento** — telemetria de sessão, crash reporting ou log de erros
* **Cobertura de testes: 50%** dos sistemas de lógica de jogo (engine, shaders, UI e assets ficam fora da contagem)

Inclua **prints do pipeline** e do relatório de cobertura.

---

## 13. Testes e Playtests

**Objetivo:** provar que o jogo foi testado com outras pessoas.

| Data | Participantes | Principais problemas |
|---|---|---|
| DD/MM/AAAA | 5 pessoas | controles confusos |
| DD/MM/AAAA | 10 pessoas | dificuldade elevada |

Em **Melhorias Implementadas**, registre problema → solução:

> Jogadores não entendiam o objetivo inicial → tutorial adicionado.

Inclua **prints ou vídeos das sessões** e gráficos simples de resultados. Volte à Seção 4 e marque quais hipóteses se confirmaram.

---

## 14. Cronograma

**Objetivo:** mostrar o plano de execução e o quanto dele foi cumprido.

Detalhe os principais milestones com datas em `DD/MM/AAAA`. Marque o que foi entregue no prazo e o que atrasou — cronograma honesto vale mais que cronograma bonito.

---

## 15. Riscos do Projeto

**Objetivo:** antecipar o que pode dar errado.

| Risco | Impacto | Mitigação |
|---|---|---|
| IA muito complexa | atraso no projeto | simplificar comportamento |
| performance baixa | experiência ruim | otimizar ou reduzir inimigos |

Revise ao longo do semestre: risco que se concretizou deve virar registro na Seção 17.

---

## 16. Limitações Conhecidas

**Objetivo:** declarar o que ficou de fora.

Liste funcionalidades planejadas e não implementadas — multiplayer, save em nuvem, fases adicionais.

Declarar limitação é sinal de maturidade. Omitir e ser descoberto na apresentação é o oposto.

---

## 17. Decisões Importantes

**Objetivo:** registrar por que o projeto virou o que virou.

| Data | Decisão | Motivo |
|---|---|---|
| DD/MM/AAAA | remover sistema de crafting | escopo muito grande |
| DD/MM/AAAA | adicionar dash | melhorar mobilidade |

Explique sempre o **motivo**. A decisão sem justificativa não ajuda quem lê o documento depois — inclusive você.

---

## 18. Créditos

**Objetivo:** cumprir as obrigações de licenciamento.

| Recurso | Fonte | Licença |
|---|---|---|
| sprites | OpenGameArt | CC0 |
| música | compositor X | CC-BY |

Todo asset externo entra aqui. Ver [Normas e Regulamentações](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/documentation/normas.md).

---

## 19. Reflexão Final

**Objetivo:** fechar o ciclo de aprendizado.

Em 1 a 3 parágrafos: principais desafios, aprendizados técnicos e o que faria diferente.

Inclua, se possível, **prints comparando as versões inicial e final** do jogo.

---

## Recomendações Gerais

### Mantenha o documento atualizado

O GDD evolui durante o desenvolvimento. Evite deixar toda a documentação para o final — o histórico de versões do documento é parte da evidência de método.

### Use elementos visuais sempre que possível

Imagens, diagramas, wireframes, prints, GIFs, mapas de nível. Jogos são sistemas visuais.

### Documente decisões, não só resultados

Explique **por que** cada decisão foi tomada. Isso é o que diferencia um GDD de uma lista de funcionalidades.

### Controle o escopo

Projetos acadêmicos devem priorizar um conceito claro, mecânicas bem implementadas e código organizado.

**Um jogo pequeno e bem feito é melhor que um jogo grande incompleto.**
