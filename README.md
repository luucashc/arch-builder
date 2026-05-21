# arch-builder

Contexto de Negócio

Repositório central de governança arquitetural e design de sistemas, focado em padronização técnica, resiliência e escalabilidade. Este projeto serve como a fonte da verdade para decisões de engenharia e diretrizes de infraestrutura AWS, garantindo que novos serviços sigam os padrões de qualidade.

Funcionalidades Técnicas

* Padronização de arquitetura através de registros formais (Architecture Decision Records).
* Governança de infraestrutura AWS com foco em resiliência, custos e performance.
* Modelagem visual sistêmica utilizando o padrão C4 Model (Níveis 1 e 2).
* Catálogo atualizado de tecnologias, linguagens e ferramentas homologadas pela engenharia.
* Integração de diretrizes de observabilidade e monitoramento centralizado.
* Versionamento e revisão por pares de decisões técnicas críticas.

Arquitetura

O projeto fundamenta-se nos seguintes princípios arquiteturais e metodológicos:

* Documentation as Code: Toda a documentação técnica é tratada como artefato de software, sendo versionada, revisada e mantida via Git.
* ADR (Architecture Decision Records): Utilização de registros estruturados para documentar o contexto, as alternativas e a justificativa das decisões técnicas, garantindo rastreabilidade histórica.
* C4 Model: Adoção do modelo C4 para representação visual, facilitando a comunicação entre diferentes níveis de stakeholders (técnicos e negócio).
* Serverless & Event-Driven First: Priorização de arquiteturas modernas e escaláveis na nuvem AWS, conforme as diretrizes de governança do repositório.

Estrutura de Pastas

* docs/adr/: Pasta que concentra os Architecture Decision Records. Cada arquivo detalha uma decisão específica de arquitetura.
* standards/: Contém as diretrizes normativas e restrições técnicas mandatórias.
    * aws-standards.md: Definições de padrões de serviços AWS, requisitos de alta disponibilidade e gestão de custos.
    * tech-stack.md: Catálogo de linguagens (Node.js, Go, Python) e ferramentas suportadas oficialmente.
* templates/: Modelos estruturados para garantir a consistência de novos artefatos técnicos.
    * adr-template.md: Estrutura base para a criação de novos ADRs.
    * c4-model-guide.md: Guia de sintaxe e estilo para diagramas Mermaid.js seguindo o C4 Model.
* GEMINI.md: Configuração de contexto e persona do assistente técnico (Sparring Architect).

Operacional

Tecnologias e Pré-requisitos

* Markdown: Linguagem principal para escrita de documentos.
* Mermaid.js: Ferramenta para renderização de diagramas de arquitetura.
* Git: Sistema de controle de versão.
* Editor de Texto: Recomendado o uso de VS Code com extensões de Markdown Preview e Mermaid.

Configuração

Por se tratar de um repositório de governança documental, não há necessidade de variáveis de ambiente (.env). As diretrizes e configurações do assistente técnico estão consolidadas no arquivo GEMINI.md.

Comandos de Execução

* git clone: Clonar o repositório para acesso local aos padrões.
* git checkout -b adr/nome-da-decisao: Criar uma nova branch para proposição de mudanças arquiteturais via Pull Request.

Conectividade

* GitHub: Repositório oficial para versionamento e colaboração.
* AWS Management Console: Gestão de recursos e infraestrutura citados nas diretrizes.
* New Relic: Plataforma de monitoramento para acompanhamento da saúde dos serviços governados.
* Squad Responsável: Time de Arquitetura e Engenharia de Plataforma.
