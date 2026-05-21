# Padrões de Infraestrutura AWS e Stack Tecnológica

## 1. Observabilidade (Mandatório)
- **Ferramenta Padrão:** **New Relic** é a solução oficial para APM, Tracing Distribuído, Logs e Monitoramento de Infraestrutura.
- **Regra:** Não sugira AWS X-Ray, CloudWatch (para visualização/APM) ou Datadog, a menos que seja estritamente necessário para uma integração legada. Todo desenho deve considerar a exportação de telemetria (OpenTelemetry/Agents) para o New Relic.

## 2. Estratégia de Mensageria e Eventos (Event-Driven First)
Nossa arquitetura prioriza fortemente a comunicação assíncrona orientada a eventos.
- **AWS SNS + SQS (Fanout):** Padrão principal para publicação de mensagens que precisam ser consumidas por múltiplos microsserviços de forma assíncrona e resiliente (garantia de entrega, retries e DLQs).
- **AWS EventBridge:** Utilizar preferencialmente para roteamento de eventos de domínio complexos, integrações de sistemas de terceiros (SaaS) ou cron jobs/schedules complexos.
- **AWS Kinesis / MSK (Kafka):** Sugerir APENAS se houver necessidade estrita de processamento de stream em tempo real, altíssima taxa de transferência (milhões de eventos) ou necessidade de replay de eventos.

## 3. Computação (Compute)
- **Containers:** AWS ECS com Fargate é o padrão para serviços web e workers de filas. Usar EKS (Kubernetes) apenas se a complexidade ou orquestração do ecossistema exigir.
- **Serverless:** AWS Lambda é altamente encorajado para processadores de eventos (consumidores de SQS/EventBridge), rotinas curtas e APIs de baixo tráfego constante. Timeout máximo recomendado: 30s.

## 4. Persistência de Dados
- **Relacional:** Amazon Aurora PostgreSQL (Serverless v2 para workloads variáveis).
- **NoSQL:** Amazon DynamoDB para altíssima performance de leitura/escrita, estado de sessão ou tabelas de eventos únicos. Atenção rigorosa aos custos de leitura/escrita escalada.
- **Cache:** Amazon ElastiCache (Redis) para diminuir carga no banco principal e acelerar leituras frequentes.