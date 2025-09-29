## Diário de Enxaqueca – Documentação

Repositório de documentação do projeto Diário de Enxaqueca, desenvolvido na disciplina Técnicas de Programação em Plataformas Emergentes / Engenharia de Software – UNB Gama.
Este repositório organiza todas as informações do projeto, incluindo MVP, backlog, regras de negócio, diagramas UML, protótipo Figma e relatórios de entrega.

## Visão Geral

O projeto Diário de Enxaqueca é uma aplicação CRUD completa para registro e acompanhamento de episódios de enxaqueca.
O objetivo da documentação é organizar e detalhar todas as fases do projeto, garantindo rastreabilidade, clareza de requisitos e suporte para desenvolvimento backend e frontend.

## Primeira Entrega

A primeira entrega contempla:

* Criação de organização no GitHub com três repositórios distintos: 
  * Documentacao - [link](https://github.com/diario-enxaqueca/documentacao)
  * Backend - [link](https://github.com/diario-enxaqueca/backend)
  * Frontend - [link](https://github.com/diario-enxaqueca/frontend)
* Definição da arquitetura do backend
  * Python/FastAPI
  * ORM SQLAlchemy
  * MySQL 
* Implementação de apenas uma história de usuário no backend:
  * HU escolhida: 1 - "Como usuário, quero criar um episódio de enxaqueca para acompanhar meus episódios"
  * Os códigos se encontram no repositório backend na pasta [source/episodio](https://github.com/diario-enxaqueca/backend/tree/main/source/episodio) seguindo o modelo MVC - Model, View e Controller.
* Ambiente do backend configurado:
  * [Dockerfile](https://github.com/diario-enxaqueca/backend/blob/main/Dockerfile), 
  * [docker-compose.yml](https://github.com/diario-enxaqueca/backend/blob/main/docker-compose.yml)
  * Banco de dados dockerizado ([init-sql](https://github.com/diario-enxaqueca/backend/blob/main/mysql-init/init.sql))
* Estrutura mínima de testes automatizados no backend:
  * apenas um teste skipado: arquivo no repositório backend [source/episodio/teste_episodio.py](https://github.com/diario-enxaqueca/backend/blob/main/source/episodio/teste_episodio.py).
* Definição da arquitetura do frontend:
  * React.js + TypeScript
* Uso do Lint - repositório backend em [pyproject.toml]()
* Documentação clara:
  * [Guia de estilo](./docs/guia-de-estilo.md) com nome do projeto, logo, paleta de cores e ícones.
  * [Protótipo](./docs/prototipo.md) de alta fidelidade no Figma
  * Definição do [MVP](./docs/mvp.md)
  * [Backlog](./docs/backlog.md) com no mínimo 10 histórias de usuário
  * [Regras de negócio](./docs/regras-de-negocio.md) documentadas
  * Diagramas UML: [Diagrama de classes](./docs/diagrama-classes.md) e [Diagrama de sequência](./docs/diagrama-sequencia.md) (extra)


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

[MIT License](./LICENSE) © [ZenildaVieira]