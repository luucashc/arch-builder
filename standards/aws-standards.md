# Padrões de Infraestrutura AWS e Stack Tecnológica

## 1. Observabilidade (Mandatório)
- **Ferramenta Padrão:** **New Relic** é a solução oficial para APM, Tracing Distribuído e Logs.
- **Regra:** Não sugira AWS X-Ray, CloudWatch (para APM) ou Datadog. Todo desenho deve considerar a exportação de telemetria para o New Relic.

## 2. Estratégia de Mensageria e Eventos (Event-Driven First)
- **AWS SNS + SQS (Fanout):** Padrão principal para comunicação assíncrona resiliente (retries e DLQs).
- **AWS EventBridge:** Para roteamento de eventos complexos ou integrações SaaS.
- **AWS Kinesis / MSK (Kafka):** Sugerir APENAS se houver necessidade estrita de milhões de eventos/segundo ou replay de eventos.

## 3. Computação (Compute)
- **Containers:** AWS ECS com Fargate é o padrão para serviços web e workers. Usar EKS (Kubernetes) apenas se a complexidade exigir.
- **Serverless:** AWS Lambda é encorajado para processadores de eventos curtos. Timeout máximo: 30s.

## 4. Persistência de Dados
- **Relacional:** Amazon Aurora PostgreSQL.
- **NoSQL:** Amazon DynamoDB para altíssima performance. Atenção rigorosa aos custos.
- **Cache:** Amazon ElastiCache (Redis) para diminuir carga no banco principal.

## 5. Segurança e Redes (Mandatório)
- **Isolamento (VPC):** APIs, Workers e Bancos de Dados NUNCA devem ter IPs públicos. Devem rodar em Subnets Privadas.
- **Exposição:** Apenas o CloudFront e Application Load Balancers (ALB) podem ficar expostos, e devem ser protegidos pelo **AWS WAF**.
- **Segredos:** Proibido o uso de arquivos `.env` com senhas em produção. Use o **AWS Secrets Manager**.