# arch-builder

## Contexto de Negócio
Repositório central de governança arquitetural e design de sistemas, atuando como o motor de contexto para os nossos Agentes de IA de Engenharia. Serve como a fonte da verdade para decisões técnicas e diretrizes de infraestrutura AWS, garantindo que a IA valide e documente novos serviços seguindo os padrões de qualidade e as melhores práticas da organização.

## Funcionalidades técnicas
* Padronização de arquitetura através de registros formais (Architecture Decision Records).
* Governança de infraestrutura AWS com foco em resiliência, custos e performance.
* Modelagem visual sistêmica utilizando o padrão C4 Model (Níveis 1 e 2).
* Catálogo atualizado de tecnologias, linguagens e ferramentas homologadas.
* Integração de diretrizes de observabilidade e monitoramento centralizado.
* Versionamento e revisão por pares de decisões técnicas críticas.

## Arquitetura
O projeto fundamenta-se nos seguintes princípios arquiteturais e metodológicos:

* **Documentation as Code:** Toda a documentação técnica é tratada como artefato de software, versionada e revisada via Git.
* **ADR (Architecture Decision Records):** Registros estruturados para documentar o contexto e justificativa de decisões técnicas.
* **C4 Model:** Modelo para representação visual, facilitando a comunicação entre stakeholders.
* **Serverless & Event-Driven First:** Priorização de arquiteturas modernas e escaláveis na nuvem AWS.

## Estrutura de Pastas
A organização do repositório segue uma lógica de separação entre diretrizes de execução, padrões técnicos e registros de decisões:

* `GEMINI.md`: Configuração central de contexto e diretrizes mandatórias para a atuação do agente Sparring Architect.
* `docs/`: Documentação técnica detalhada e guias de suporte ao usuário.
    * `adr/`: Pasta contendo os Architecture Decision Records (ADRs) que documentam o histórico e evolução técnica.
    * `how-to-use.md`: Guia prático de comandos e melhores práticas para interação com o agente.
* `standards/`: Camada normativa contendo as definições de governança e restrições.
    * `aws-standards.md`: Define os padrões de infraestrutura, segurança, resiliência e custos para serviços AWS.
    * `c4-model-guide.md`: Regras de sintaxe e estilo obrigatórias para a geração de diagramas de arquitetura (Mermaid).
    * `tech-stack.md`: Catálogo atualizado de tecnologias e linguagens homologadas pela engenharia.
* `templates/`: Repositório de modelos estruturais para garantir a padronização de novos artefatos.
    * `adr-template.md`: Estrutura base inegociável para a criação de novos registros de decisão arquitetural.

## Operacional

### Tecnologias/Pré-requisitos
* Markdown (Linguagem de marcação para os documentos)
* Mermaid.js (Motor de renderização de diagramas)
* Git (Controle de versão)
* Editor de Texto (VS Code recomendado com extensões para Markdown e Mermaid)

### Configuração
Este repositório não utiliza variáveis de ambiente ou arquivos `.env`. Todas as configurações de diretrizes estão contidas no arquivo `GEMINI.md`. Certifique-se de que o contexto do repositório está carregado no Gemini CLI.

Para detalhes sobre como interagir com o agente e exemplos de comandos, consulte o guia prático em: [how-to-use.md](docs/how-to-use.md).

## Conectividade
* **GitHub:** [Repositório Oficial](https://github.com/luucashc/arch-builder)
