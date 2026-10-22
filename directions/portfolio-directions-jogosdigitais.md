# Linha de Projeto – Jogos Digitais

## O que é obrigatório atender
Requisitos mínimos e obrigatórios para habilitação ao Poster + Demo Day.

- O jogo deve ser jogável do início ao fim, com ao menos uma fase ou loop completo funcional.
- Build funcional distribuída (ex.: executável standalone, WebGL hospedado, APK, ou link para plataforma de testes).

> **O que é “ambiente produtivo” em Jogos:** o [Portfolio.md](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md) exige aplicação hospedada em nuvem, pública e estável. Para esta linha, o equivalente é a **build pública e distribuída** — Itch.io, loja, WebGL hospedado ou APK com link direto. O que não é aceito é build que só roda na máquina do autor ou que dependa dele para ser executada no dia da apresentação.
>
> **Onde hospedar o WebGL:** Itch.io, loja ou servidor próprio. **Vercel, Netlify e Render estão 🚫 Não Usar desde 2026-02**, sem exceção para esta linha — ver o [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md).
- Código-fonte acessível em repositório público ou privado com acesso autorizado aos professores avaliadores — esta linha é a **única exceção** à exigência de repositório público, em função de assets licenciados e de requisitos de publicação em loja.
- Documentação com foco em game design: visão geral do jogo, objetivo principal, loop central de gameplay, mecânicas implementadas e tecnologias utilizadas — estruturada no [Template de GDD](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/documentation/games/GDD%20-%20Template.md), com apoio do [Guia de Preenchimento](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/documentation/games/GuiaPreenchimenteBoasPraticas.md).
- Apresentação de elementos mínimos de jogabilidade: personagem/jogador controlável, regras, objetivo, vitória/derrota.
- Interface minimamente navegável (menus, HUD, feedbacks visuais ou sonoros).
- Arte e som podem ser placeholders, mas precisam representar a intenção do design.
- **Playtest** com no mínimo 10 participantes, na noite oficial ou de forma independente com evidências, e **relatório do playtest** entregue no prazo, conforme as [Diretrizes de Playtest](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/documentation/games/Diretrizes-Playtest.md). Datas no [Calendário](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/calendario.md).

### Núcleo comum de engenharia

Requisitos válidos para **todas as linhas de projeto**, conforme o [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md):

- **Documentação em Wiki** junto ao repositório (Wiki do GitHub ou equivalente).
- **Pipeline CI/CD** com build automatizado a cada entrega (ex.: GitHub Actions, Unity Cloud Build).
- **Análise estática de código** (ex.: SonarQube, SonarCloud, analisadores da própria engine).
- **Monitoramento** — telemetria básica de sessão, crash reporting ou log de erros da build publicada.

> **Testes nesta linha:** não há meta de cobertura obrigatória. Em jogos, boa parte do comportamento depende de engine, cena e tempo real, e uma meta percentual incentiva teste raso — ver *O que é desejável atender*. TDD é ✅ recomendado, não obrigatório.

---

## O que é desejável atender
- **GDD completo** — todas as seções do template preenchidas, incluindo hipóteses de design, prototipagem, riscos e registro de decisões. O GDD mínimo (visão, loop, mecânicas, tecnologias) já é **obrigatório**; o que é desejável aqui é o documento completo e mantido vivo ao longo do semestre.
- Design visual e sonoro consistente com a proposta do jogo.
- Implementação de feedback tátil, visual e/ou sonoro (game feel).
- Uso de engine consolidada no mercado (Unity, Unreal, Godot, etc.) ou criação da própria engine.
- Build publicada em plataforma de acesso público (ex.: Itch.io, Steam em acesso antecipado, Google Play em beta) com o jogo completo - todas as fases, todo o conteúdo.
- Suporte a diferentes resoluções e dispositivos (caso multiplataforma).
- Testes automatizados dos sistemas de lógica de jogo (regras, progressão, estado), fora o código de engine, shaders, UI e assets.

---

## O que é um diferencial
- Implementação de sistemas de progressão, IA, física personalizada, multiplayer ou mecânicas emergentes.
- Playtests com público externo, além do playtest obrigatório com colegas, e iteração baseada em feedback real.
- Experiência polida com foco em imersão, ritmo e curva de dificuldade.
- Design original de arte, som e narrativa integrada ao gameplay.
- Lançamento efetivo em loja/plataforma ou marketing ativo.

---

## O que deve ser evitado
- Cópia direta de tutoriais sem personalização.
- Mecânicas desconexas ou sem clareza no objetivo do jogador.
- Bugs que comprometem a experiência de jogo (ex.: quedas de FPS, travamentos, impossibilidade de completar a fase).
- Interface poluída ou ausente, dificultando navegação ou entendimento.

---

## O que não pode ter
- Projeto com apenas mockups ou trailer sem jogabilidade funcional.
- Plágio de jogos existentes com assets e código copiados sem modificação.
- Experiência de jogo inexistente ou sem interação (ex.: apenas uma cutscene, apenas menus).
- Falta completa de regras ou condições de jogo.
- Quebra do ciclo de jogo: sem condição de vitória/derrota, ou sem ações significativas do jogador.

---

## Temas a evitar

Valem os temas marcados ⚠️ **Evitar** na tabela do [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md) — recorrentes ou de alta concorrência. Não impedem a aprovação, mas exigem diferencial claro para se sustentarem.

---

## Temas impedidos

Valem os temas marcados 🚫 **Não Usar** na tabela do [Portfólio Directions](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/directions/portfolio-directions-GERAL.md), somados aos itens de *O que não pode ter* desta linha — em especial clones de jogos existentes com assets e código copiados sem modificação.

---

## Régua de Avaliação

- **Destaque** — além de todos os obrigatórios, o projeto tem gameplay consistente, polimento, diferencial técnico ou criativo, e evidência de iteração a partir de playtests. Concorre a menção de destaque e a convite para a **Banca Técnica Especial**.
- **Aprovado** — atende a **todos** os itens *obrigatórios*, incluindo o núcleo comum de engenharia: jogo funcional com ao menos um loop completo, build pública distribuída, GDD mínimo coerente e playtest com relatório. Nota final igual ou superior a **6,0**.
- **Reprovado** — não apresenta jogabilidade mínima funcional, incorre em item de *“o que não pode ter”*, ou obtém nota final abaixo de **6,0**.
