## Diário de Enxaqueca – Documentação

Repositório de documentação do projeto Diário de Enxaqueca, desenvolvido na disciplina Técnicas de Programação em Plataformas Emergentes / Engenharia de Software – UNB Gama.
Este repositório organiza todas as informações do projeto, incluindo MVP, backlog, regras de negócio, diagramas UML, protótipo Figma e relatórios de entrega.

## Visão Geral

O projeto Diário de Enxaqueca é uma aplicação CRUD completa para registro e acompanhamento de episódios de enxaqueca.
O objetivo da documentação é organizar e detalhar todas as fases do projeto, garantindo rastreabilidade, clareza de requisitos e suporte para desenvolvimento backend e frontend.

## Primeira Entrega

A primeira entrega contempla:

* Criação de comunidade no GitHub com três repositórios distintos: [documentacao](https://github.com/diario-enxaqueca/documentacao), [backend](https://github.com/diario-enxaqueca/backend), [frontend](https://github.com/diario-enxaqueca/frontend)
* Backend funcional com FastAPI + SQLAlchemy + MySQL (para somente uma regra de negócio)
* Frontend com React.js + TypeScript (apenas a criação do repositório separado)
* Estrutura mínima de testes automatizados (apenas um teste skipado no backend)
* Documentação clara em repositório separado 
  * [Guia de estilo](./docs/guia-de-estilo.md) com logo, paleta de cores e ícones.
  * [Protótipo](./docs/prototipo.md) de alta fidelidade no Figma
  * Definição do [MVP](./docs/mvp.md)
  * [Backlog](./docs/backlog.md) com no mínimo 10 histórias de usuário
  * [Regras de negócio](./docs/regras-de-negocio.md) documentadas
  * Diagramas UML: [Diagrama de classes](./docs/diagrama-classes.md) e [Diagrama de sequência](./docs/diagrama-sequencia.md) (extra)



## Estrutura da Documentação

```code
documentacao/
│
├── assets
│   ├── historias_usuario/   # Detalhes de cada história de usuário
├── assets
├── regras_negocio/      # Documento com regras de negócio e validações
├── uml/                 # Diagramas UML
├── prototipo_figma/     # Links, capturas de tela e documentação do protótipo
├── relatorios/          # Relatórios de entregas e acompanhamento
├── CONTRIBUITNG.md
├── LICENSE
└── README.md
```

## Contribuição

Contribuições são bem-vindas! Para manter consistência e qualidade na documentação, siga as instruções detalhadas no arquivo [CONTRIBUTING.md](CONTRIBUTING.md).

Ele inclui orientações sobre:
* Clonar o repositório
* Criar branch a partir da `main`
* Padrão de commits (**Conventional Commits**)
* Abrir Pull Requests com descrição clara
* Boas práticas de **pastas**, **UML**, **backlog**, **regras de negócio** e **protótipo Figma**

Obrigado por ajudar a manter a documentação do Diário de Enxaqueca clara e completa!

## Licença

MIT License © [ZenildaVieira]