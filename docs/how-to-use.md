# Como usar o Agente de Arquitetura (Sparring Architect)

Este agente não é um gerador mágico de código. Ele é um **Staff Engineer Virtual** projetado para debater ideias, encontrar falhas no seu raciocínio e documentar a decisão final. 

Para extrair o melhor dele, siga estas 4 regras de ouro:

## Regra 1: Traga o Problema, não a Solução fechada
**Mau uso (Brain dump):** *"Cria um C4 model pra mim de um sistema que pega arquivo do S3, joga num Lambda, salva no Dynamo e depois manda um email usando Kafka."* (O agente vai tentar desenhar essa bagunça, mesmo que Kafka não faça sentido aqui).

**Bom uso:** *"Preciso criar um serviço de upload de faturas que suporte 10.000 envios por hora. Quando a fatura chega, precisamos ler os dados dela e notificar o usuário. Como podemos desenhar isso na AWS?"*

## Regra 2: Responda a "Fase 0" com atenção
A IA vai te fazer perguntas (Volumetria, SLA, Segurança). Não pule essas perguntas. Responda-as claramente, pois elas definem se a IA vai sugerir um serviço simples (Lambda) ou um cluster complexo (ECS/SQS).

## Regra 3: O Refactoring ("Sparring")
A primeira sugestão da IA **nunca é a versão final**. Debata com ela!
* *"Achei essa arquitetura com EventBridge cara. Tem como simplificar?"*
* *"O time só sabe Node.js, não queremos usar Go. Refaça o design."*

## Regra 4: A Consolidação
Só peça o diagrama e o documento quando vocês chegarem a um acordo. Quando estiver satisfeito com o fluxo, envie:
* *"Perfeito. Fechamos a arquitetura. Por favor, gere o ADR e o C4 Model seguindo os padrões do repositório."*