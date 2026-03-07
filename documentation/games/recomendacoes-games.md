
# Documentação do Projeto — Games.pdf

## 1. Documentação do Projeto

**Alternativa à Wiki do Repositório:** A sugestão é a utilização de um **Game Design Document (GDD)** integrado com ferramentas como Notion, Miro, Obsidian ou HacknPlan, mantendo o controlo de versionamento da documentação.

**Justificação:** Jogos requerem documentação visual e interativa (mapas, fluxogramas de mecânicas, wireframes e storyboards).

**Papel do GDD:** É o núcleo do projeto e deve ser versionado para acompanhar o histórico de decisões e revisões.


### Ferramentas Recomendadas:
  
**Notion:** Estrutura modular para documentação interativa.

**Miro:** Diagramas, fluxos de gameplay e brainstorms visuais.

**Obsidiana:** Gestão de notas interconectadas para narrativa e design.

**HacknPlan:** Gestão ágil focada em jogos.

**Perforce (P4) / Plastic SCM / Git LFS:** Controlo de versão de assets e do GDD.

**Estrutura do GDD:** Deve conter Visão Geral, História e Narrativa, Mecânicas e Gameplay, Interface e HUD, Arte e Sons, e Histórico de Versões.


## 2. Controlo de Código e Versionamento

**Alternativa ao CI/CD Tradicional:** Controlo de código-fonte, versionamento do GDD e deploy manual em plataformas.

**Justificação:** Builds automatizadas e CI/CD convencional não são viáveis devido à natureza iterativa dos jogos.

**Estratégia de Deploy:** Deve ser controlado manualmente, respeitando os estágios Alpha, Beta e Release.



### Ferramentas Práticas:

**Perforce / Plastic SCM:** Melhor controlo para código e assets.

**Git LFS (Large File Storage):** Armazenamento de modelos 3D, texturas e animações sem prejudicar a performance do repositório.

**Sistemas de Deploy:** Itch.io Butler, Steamworks SDK ou Epic Online Services para upload manual.

**Fluxo de Trabalho:** Commit (Código + GDD) -> Controlo de revisão -> Testes internos e playtesting -> Distribuição manual.



## 3. Ciclo de Testes e Playtesting

**Alternativa ao TDD:** Playtesting Estruturado e Escalonamento de Testes (Vertical Slice → Alpha → Beta).

**Justificação:** O fluxo não é fixo; elementos como *game feel*, física e IA emergente não são validados apenas com testes unitários.


### Fases de Teste:

**Vertical Slice:** Recorte representativo do jogo testado internamente.

**Alpha:** Grupo pequeno de testadores internos com debugging ativo.

**Beta:** Grupo alargado de jogadores reais para recolha de feedback e métricas.

**Ferramentas de QA e Bugs:** JIRA, Trello ou HacknPlan para controlo de tarefas.


### Automação e Telemetria
Unity Test Framework ou Unreal Automation para física/scripts; Unity Analytics ou Playfab para dados reais dos jogadores.



### Tabela de Controlo de QA e Bugs (Exemplo)

| ID | Descrição | Severidade | Status | Responsável |
| --- | --- | --- | --- | --- |
| BUG-001 | Animação do personagem travando ao pular | Alta | Em andamento | Dev de Animação |
| BUG-002 | Áudio cortando ao mudar de cena | Média | Resolvido | Dev de Áudio |
| BUG-003 | FPS caindo abaixo de 30 em certas áreas | Crítica | Pendente | Dev de Performance |
 |  |  |  |  |

## 4. Conclusão

* Conceitos tradicionais (Wiki, CI/CD, TDD) devem ser substituídos por práticas adaptadas à natureza experimental do desenvolvimento de jogos.
* 
* O foco deve recair sobre documentação visual, rastreio de versões de código e GDD, testes escalonados e QA baseado em dados de jogadores reais.
* 
* Este modelo garante agilidade, colaboração e centralidade na experiência do jogador, permitindo o uso de qualquer engine sem restrições.

