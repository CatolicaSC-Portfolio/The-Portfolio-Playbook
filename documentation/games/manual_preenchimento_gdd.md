# Manual de Preenchimento: Game Design Document (GDD) e Recomendações

Este manual orienta o estudante na substituição da Wiki, CI/CD e TDD tradicionais por práticas adaptadas à natureza iterativa do desenvolvimento de jogos digitais.

## 1. Guia de Preenchimento do GDD Template

Diferente de sistemas de gestão, jogos exigem uma documentação visual e interativa. O GDD é o núcleo do projeto e deve ser versionado.

### Seções do Template:

* **Visão Geral do Jogo:**
* **Tema e Gênero:** Defina o universo do jogo e seu estilo (Ex: Plataforma 2D, RPG por turnos).
* **Público-Alvo:** Identifique para quem o jogo está sendo construído.
* **Objetivo Principal:** O que o jogador deve alcançar para concluir o loop básico (obrigatório: ter ao menos uma fase ou loop completo funcional).


* **História e Narrativa:**
* **Personagens e Lore:** Descreva o protagonista e o contexto do mundo. Mesmo em jogos simples, o contexto é um diferencial para a imersão.


* **Mecânicas e Gameplay:**
* **Core Loop:** Detalhe o ciclo "Ação -> Desafio -> Recompensa".
* **Regras e Controles:** Liste as leis que regem o mundo e como o jogador interage (obrigatório: personagem controlável e regras claras).
* **Condições de Vitória/Derrota:** Defina o que encerra o ciclo de jogo (requisito obrigatório).


* **Interface e HUD:**
* **Mockups e Navegação:** Inclua wireframes das telas (Menu, Pause, Game Over) e elementos visuais em tela (vida, munição, etc.).


* **Arte e Sons:**
* **Direção Visual e Áudio:** Descreva o estilo artístico (Pixel art, Low poly). Arte e som podem ser *placeholders* (temporários), mas devem representar a intenção do design.


* **Histórico de Versões do GDD:**
* Registre as mudanças e revisões controladas para acompanhar a evolução das decisões de design.



---

## 2. Manual de Práticas e Recomendações Técnicas

Para jogos, as ferramentas tradicionais de software são substituídas por fluxos que priorizam o *game feel* e o versionamento de *assets* pesados.

### Controle de Código e Assets (Alternativa ao CI/CD)

* **Versionamento:** Utilize **Git LFS (Large File Storage)**, Perforce (P4) ou Plastic SCM para gerenciar texturas, modelos 3D e o próprio GDD sem afetar a performance do repositório.
* **Deploy Manual:** O deploy não deve ser totalmente automatizado via pipeline tradicional. Deve ser controlado manualmente respeitando as fases **Alpha, Beta e Release**.
* **Distribuição:** Utilize plataformas como **Itch.io (via Butler)**, Steamworks SDK ou Epic Online Services para o upload das builds funcionais.

### Ciclo de Testes e Playtesting (Alternativa ao TDD)

O TDD é ineficiente para validar física ou IA emergente. Substitua-o pelo escalonamento de testes:

1. **Vertical Slice:** Teste interno de um pequeno recorte funcional que contenha todas as mecânicas centrais.
2. **Playtesting Alpha:** Testes com um grupo restrito (QA e desenvolvedores) focado em depuração (*debugging*).
3. **Playtesting Beta:** Testes com jogadores externos reais para coleta de métricas e feedback de experiência.

---

## 3. Registro de Qualidade (QA e Bugs)

É obrigatório manter uma tabela de controle de bugs no repositório para evidenciar a engenharia de qualidade.

| Campo | Descrição do Preenchimento |
| --- | --- |
| **ID** | Código único (Ex: BUG-001). |
| **Descrição** | Detalhe o erro encontrado (Ex: "Colisão falhando na borda da fase"). |
| **Severidade** | Classifique como Crítica (impede o jogo), Alta, Média ou Baixa. |
| **Status** | Pendente, Em andamento ou Resolvido. |
| **Responsável** | Nome do integrante que fará a correção. |

### Ferramentas de Apoio Sugeridas:

* **Gestão Visual:** Miro ou Notion para o GDD.
* **Gerenciamento Ágil:** HacknPlan (específico para games).
* **Métricas:** Unity Analytics ou Playfab para coletar dados reais de uso dos jogadores.
