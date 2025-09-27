## Diário de Enxaqueca – Documentação

Repositório de documentação do projeto Diário de Enxaqueca, desenvolvido na disciplina Técnicas de Programação em Plataformas Emergentes / Engenharia de Software – UNB Gama.
Este repositório organiza todas as informações do projeto, incluindo MVP, backlog, regras de negócio, diagramas UML, protótipo Figma e relatórios de entrega.

## Índice

* Visão Geral
* MVP
* Backlog e Regras de Negócio
* Diagramas UML
* Protótipo Figma
* Estrutura da Documentação
* Entrega da Primeira Etapa
* Contribuição
* Licença

## Visão Geral

O projeto Diário de Enxaqueca é uma aplicação CRUD completa para registro e acompanhamento de episódios de enxaqueca.
O objetivo da documentação é organizar e detalhar todas as fases do projeto, garantindo rastreabilidade, clareza de requisitos e suporte para desenvolvimento backend e frontend.

## MVP

O MVP da primeira entrega contempla:

* CRUD completo de registros de enxaqueca
* Backend funcional com FastAPI + SQLAlchemy + MySQL
* Frontend funcional com React.js + TypeScript
* Protótipo de alta fidelidade no Figma
* Estrutura mínima de testes automatizados
* Documentação clara de backlog, regras de negócio e UML

## Backlog e Regras de Negócio

10 Histórias de Usuário simplificadas:
| #  | História de Usuário         | Regras de Negócio                                           |
| -- | --------------------------- | ----------------------------------------------------------- |
| 1  | Cadastro de usuário         | E-mail único, senha segura                                  |
| 2  | Login                       | Autenticação via JWT                                        |
| 3  | Criar registro de enxaqueca | Campos: data, intensidade, gatilhos, medicação, observações |
| 4  | Listar registros            | Apenas registros do usuário logado                          |
| 5  | Atualizar registro          | Permitir edição de todos os campos                          |
| 6  | Excluir registro            | Exclusão física                                             |
| 7  | Documentação da API         | Swagger automático                                          |
| 8  | Testes unitários            | Pytest para endpoints CRUD                                  |
| 9  | Protótipo visual            | Alta fidelidade implementada fielmente                      |
| 10 | Deploy com Docker           | Backend e MySQL dockerizados                                |

Cada história de usuário é detalhada em documento individual dentro da pasta `historias_usuario/`.

## Diagramas UML

Para a primeira entrega, foram criados os seguintes diagramas UML:

* Diagrama de classes – Estrutura do backend e relações entre modelos
* Diagrama de sequência – Fluxo do CRUD de registros de enxaqueca
* Diagrama de casos de uso – Interações do usuário com o sistema

Os arquivos estão disponíveis em `uml/` no formato PDF e PNG.

## Protótipo Figma

O protótipo de alta fidelidade está disponível em [Figma]() e em `prototipo_figma/` no formato PDF.

* Segue layout, paleta de cores, ícones autoexplicativos e fluxo definido no MVP
* Componentes, formulários e telas de CRUD implementados conforme protótipo

## Estrutura da Documentação

```code
diario-enxaqueca-documentacao/
│
├── historias_usuario/   # Detalhes de cada história de usuário
├── regras_negocio/      # Documento com regras de negócio e validações
├── uml/                 # Diagramas UML
├── prototipo_figma/     # Links, capturas de tela e documentação do protótipo
├── relatorios/          # Relatórios de entregas e acompanhamento
└── README.md
```

## Entrega da Primeira Etapa

Para a primeira entrega, estão incluídos:

1. Definição do MVP
2. Backlog com 10 histórias de usuário
3. Regras de negócio documentadas
4. Diagramas UML (classes, sequência, casos de uso)
5. Protótipo de alta fidelidade no Figma
6. Estrutura inicial de testes (skipado apenas para demonstrar)

Todos os arquivos e links estão organizados no repositório, facilitando a avaliação e continuidade do desenvolvimento.

## Contribuição

1. Fork do repositório
2. Criar branch (git checkout -b feature/nova-documentacao)
3. Commit (git commit -m "Adiciona documentação da X")
4. Push (git push origin feature/nova-documentacao)
5. Abrir Pull Request

## Licença

MIT License © [ZenildaVieira]