# Stack Tecnológica Homologada

## 1. Backend / Serviços
- **Node.js (TypeScript):** Stack principal para APIs I/O-bound, BFFs e Lambdas rápidos.
- **Go (Golang):** Usar para serviços de alta performance, processamento de streams ou componentes críticos de infraestrutura.
- **Python:** Restrito a processamento de dados, IA/ML, e scripts de automação.

## 2. Mensageria
- Preferir **AWS SQS** para filas simples e desacoplamento.
- Usar **AWS EventBridge** para arquiteturas orientadas a eventos (Event-Driven).
- Evitar Kafka/MSK a menos que o volume de streaming justifique o custo operacional.

## 3. Estratégia de Testes (Obrigatório)
- **Testes Unitários:** Mandatório. (Jest/Vitest para Node; pacote nativo `testing` para Go).
- **Testes de Integração:** O design deve prever o uso de mocks/stubs ou Testcontainers para APIs externas e bancos.
- **Testes de Carga:** Arquiteturas críticas devem prever testes com K6 antes de ir para produção.

## 4. Padrões de Logs
- Todos os logs devem ser estritamente em formato **JSON**.
- Toda requisição/mensagem deve carregar um `Correlation-ID` no cabeçalho para rastreabilidade fim-a-fim.