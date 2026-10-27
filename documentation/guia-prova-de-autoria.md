# Guia de Preparação para a Prova de Autoria

A **prova de autoria** é o último encontro da [Disciplina de Portfólio](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md#prova-de-autoria). Nela o professor questiona você, individualmente, sobre o seu projeto, para confirmar que o trabalho é de autoria genuína.

Este guia reúne **perguntas típicas** da prova, organizadas por aspecto do projeto. Use-o para se preparar: abra o seu repositório e responda cada uma **mostrando o código**.

> **Atenção:** esta não é uma lista fechada. O professor pode fazer outras perguntas, aprofundar qualquer resposta com "por quê?" e "e se…?" e pedir alterações no código durante a prova. As regras oficiais estão em [Portfolio.md § Prova de Autoria](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/Portfolio.md#prova-de-autoria); em caso de divergência, vale o que está lá.

---

## O que é verificado

- **Conhecimento do codebase**: você sabe onde as coisas estão, o que cada parte faz e por que está escrita daquele jeito.
- **Decisões de engenharia**: você justifica a arquitetura, as tecnologias escolhidas, os padrões aplicados e os trade-offs assumidos.
- **Domínio do trabalho**: você explica o que construiu sem depender de anotações ou de terceiros.
- **Cobertura de testes, apenas na linha de Web Apps** (e no backend próprio de um projeto Mobile): meta de **75% no backend e 25% no frontend**. Nas linhas de Mobile, IA, IoT e Jogos Digitais não há meta de cobertura.

O uso de assistentes de IA no desenvolvimento não é proibido, mas **não dispensa o domínio do resultado**: você responde por cada decisão e por cada linha do que entregou.

---

## Perguntas típicas

As perguntas foram escritas pensando em um sistema com back-end e interface. Se o seu projeto é de outra linha, adapte o sentido: em **Mobile**, "front-end" é o app; em **IoT**, inclui firmware, sensores e o protocolo de comunicação; em **IA**, inclui o pipeline de dados e o modelo; em **Jogos Digitais**, a "regra de negócio" é a lógica de jogo e o "deploy" é a build pública.

### Arquitetura e decisões

1. Desenhe a arquitetura do projeto: quais componentes existem e por onde passa uma requisição, do clique do usuário até o banco de dados?
2. Por que você escolheu essa stack (linguagem, framework, banco)? Qual alternativa foi descartada e por quê?
3. Onde fica o ponto de entrada da aplicação (`main`, `index`, `app`) e o que acontece na inicialização?

### Configuração e ambiente

4. Onde é feita a configuração de conexão com o banco de dados? O que muda entre o ambiente de desenvolvimento e o de produção?
5. Quais variáveis de ambiente o projeto precisa? Em que ponto do código elas são lidas e onde ficam guardadas em produção?
6. Se eu clonar o repositório agora, quais passos exatos preciso seguir para rodar o projeto localmente?

### Dados

7. Quais são as entidades principais e como elas se relacionam? Onde isso está definido no código (models, schema, migrations)?
8. Mostre a última migration (ou alteração de schema) e explique o que ela faz.
9. Em qual trecho do código é feito o filtro por usuário, ou seja, o que impede um usuário de ver os dados de outro?

### Autenticação e segurança

10. Como é feita a autenticação? Onde o token ou a sessão é gerado, onde é validado e quando expira?
11. Como funciona a autorização? Mostre onde uma rota ou tela é bloqueada para quem não tem permissão.
12. Como as senhas e os dados sensíveis são armazenados? O que protege os seus formulários contra SQL injection ou XSS?

### Regras de negócio e fluxo

13. Abra o arquivo da funcionalidade principal e explique, linha a linha, a regra de negócio que ele implementa.
14. O que acontece se o usuário enviar um dado inválido em um formulário? A validação está no front-end, no back-end ou nos dois?
15. Como os erros são tratados e registrados? Se uma operação falhasse em produção, onde você veria o erro?

### Integrações

16. Como o front-end (ou o app, ou o dispositivo) se comunica com o back-end? Mostre onde a chamada é feita e onde a resposta é tratada.
17. O projeto usa alguma API ou serviço externo? Onde está essa integração e o que acontece se o serviço sair do ar?

### Testes e qualidade

18. Quais testes existem? Rode-os agora e explique o que um deles verifica. Em **Web Apps**, mostre também o relatório de cobertura.
19. Se eu mudar uma regra de negócio, qual teste deveria falhar? Faça a mudança e mostre.

### CI/CD e deploy

20. O que seria preciso alterar no CI/CD para executar as integrações manualmente, e não automaticamente a cada merge?
21. Quais etapas o pipeline roda, em que ordem, e o que acontece quando um teste ou a análise estática falha?
22. Onde a aplicação está hospedada e como é feito o deploy? Como você voltaria para a versão anterior se uma versão com problema fosse publicada?

### Processo e histórico

23. Escolha um commit seu no histórico do Git e explique o que mudou e por quê. Qual foi o pull request mais difícil que você revisou ou teve revisado no seu squad?
24. Qual foi o bug mais difícil do projeto? Como você descobriu a causa e onde está a correção?

### Mudança ao vivo

25. Adicione agora um campo novo a uma entidade e faça ele aparecer na tela. Explique o que precisou mudar em cada camada.

---

## Checklist antes da prova

- [ ] Consigo responder todas as perguntas acima **navegando no meu próprio código**, sem depender da busca global da IDE.
- [ ] O projeto roda localmente na minha máquina e eu sei explicar cada passo do setup.
- [ ] Sei explicar cada dependência relevante do projeto e por que ela está ali.
- [ ] Sei explicar todo trecho gerado com apoio de IA tão bem quanto o que escrevi sozinho.
- [ ] Consigo fazer uma pequena alteração ao vivo (novo campo, nova validação) e rodar os testes em seguida.
- [ ] **Web Apps:** a cobertura está em pelo menos 75% no backend e 25% no frontend, e eu sei gerar o relatório.

---

## Prazos e consequências

- A prova é **individual** e ocorre até **30/11/2026 (segunda-feira)**, junto com o prazo de entrega.
- A aprovação é **condição para se habilitar ao Poster + Demo Day**. Sem ela, o trabalho não é considerado entregue.
- Quem reprova, por qualquer item verificado (inclusive a cobertura de testes), tem direito a **uma segunda tentativa**, até **03/12/2026 (quinta-feira)**.
- Reprovando na segunda tentativa, o aluno está **reprovado na disciplina** e não participa do Poster + Demo Day.
- Autoria é o critério 5 do [Guia de Avaliação](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/demoday/Avaliacao_Poster_DemoDay.md) e é **eliminatório**: plágio ou falsificação resultam em reprovação imediata.

Todas as datas seguem o [Calendário 2026/2](https://github.com/CatolicaSC-Portfolio/The-Portfolio-Playbook/blob/main/calendario.md).
