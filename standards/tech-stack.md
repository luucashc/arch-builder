# Stack Tecnológica Homologada

## Backend / Serviços
- **Node.js (TypeScript):** Stack principal para APIs I/O-bound, BFFs e Lambdas rápidos.
- **Go (Golang):** Usar para serviços de alta performance, processamento de streams ou componentes críticos de infraestrutura.
- **Python:** Restrito a processamento de dados, IA/ML, e scripts de automação.

## Mensageria
- Preferir **AWS SQS** para filas simples e desacoplamento.
- Usar **AWS EventBridge** para arquiteturas orientadas a eventos (Event-Driven).
- Evitar Kafka/MSK a menos que o volume de streaming justifique o custo operacional.
