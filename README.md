# arch-builder

## Contexto de Negócio

Repositório central de governança arquitetural e design de sistemas, que atua como o motor de contexto para os nossos Agentes de IA de Engenharia. Este projeto serve como a fonte da verdade para decisões técnicas e diretrizes de infraestrutura AWS, garantindo que a IA valide e documente novos serviços seguindo os padrões de qualidade e as melhores práticas de nuvem da organização.

## Funcionalidades Técnicas

* Padronização de arquitetura através de registros formais (Architecture Decision Records).
* Governança de infraestrutura AWS com foco em resiliência, custos e performance.
* Modelagem visual sistêmica utilizando o padrão C4 Model (Níveis 1 e 2).
* Catálogo atualizado de tecnologias, linguagens e ferramentas homologadas pela engenharia.
* Integração de diretrizes de observabilidade e monitoramento centralizado.
* Versionamento e revisão por pares de decisões técnicas críticas.

## Arquitetura

O projeto fundamenta-se nos seguintes princípios arquiteturais e metodológicos:

* Documentation as Code: Toda a documentação técnica é tratada como artefato de software, sendo versionada, revisada e mantida via Git.
* ADR (Architecture Decision Records): Utilização de registros estruturados para documentar o contexto, as alternativas e a justificativa das decisões técnicas.
* C4 Model: Adoção do modelo C4 para representação visual, facilitando a comunicação entre diferentes níveis de stakeholders.
* Serverless & Event-Driven First: Priorização de arquiteturas modernas e escaláveis na nuvem AWS.

## Estrutura de Pastas

```text
/
├── docs/               # Documentação técnica detalhada
│   └── adr/            # Architecture Decision Records (ADRs)
├── standards/          # Diretrizes e restrições técnicas mandatórias
├── templates/          # Modelos para novos artefatos técnicos
└── GEMINI.md           # Configuração de contexto do Sparring Architect
```

## Detalhamento Técnico

* docs/adr/: Concentra os Architecture Decision Records. Cada arquivo detalha uma decisão específica de arquitetura, garantindo rastreabilidade histórica das escolhas técnicas.
* standards/: Contém as diretrizes normativas. O arquivo `aws-standards.md` define padrões de alta disponibilidade e custos, enquanto o `tech-stack.md` cataloga linguagens suportadas (Node.js, Go, Python).
* templates/: Modelos estruturados para garantir consistência. Inclui o `adr-template.md` para novos registros e o `c4-model-guide.md` para diagramas Mermaid.js.

## Operacional

### Tecnologias e Pré-requisitos

* Markdown: Escrita de documentos.
* Mermaid.js: Renderização de diagramas.
* Git: Controle de versão.
* Editor: VS Code (recomendado extensões de Markdown e Mermaid).

### Configuração

Por ser um repositório de governança documental, não utiliza variáveis de ambiente (.env). As diretrizes de interação do assistente técnico estão no `GEMINI.md`.

## Conectividade

* GitHub: [Repositório Oficial](https://github.com/luucashc/arch-builder)
* Monitoramento: [New Relic Dashboard](https://one.newrelic.com)
