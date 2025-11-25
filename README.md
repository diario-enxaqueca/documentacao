# Diário de Enxaqueca

Sistema de gerenciamento de crises de enxaqueca com backend FastAPI, autenticação JWT e frontend React.

Repositório de documentação do projeto Diário de Enxaqueca, desenvolvido na disciplina Técnicas de Programação em Plataformas Emergentes / Engenharia de Software – UNB Gama.
Este repositório organiza todas as informações do projeto, incluindo MVP, backlog, regras de negócio, diagramas UML, protótipo Figma e relatórios de entrega.

## Visão Geral

O projeto Diário de Enxaqueca é uma aplicação CRUD completa para registro e acompanhamento de episódios de enxaqueca.
O objetivo da documentação é organizar e detalhar todas as fases do projeto, garantindo rastreabilidade, clareza de requisitos e suporte para desenvolvimento backend e frontend.

## Arquitetura do Projeto

O projeto é composto por 4 componentes principais, orquestrados via Docker Compose:

- **Backend** (`backend/`): API REST desenvolvida com FastAPI (Python), utilizando SQLAlchemy como ORM e MySQL como banco de dados. As rotas são registradas em `backend/main.py` sob o prefixo `/api/*`.
- **Autenticação** (`autenticacao/`): Serviço separado de autenticação JWT, construído com FastAPI. Atualmente, o `docker-compose.yml` refere-se a um serviço `auth` com build `./auth`, mas o diretório `./auth` não existe — recomenda-se ajustar para `./autenticacao`.
- **Frontend** (`frontend/`): Interface de usuário desenvolvida com React + Vite. O `package.json` define scripts `dev` e `build`. Não possui Dockerfile atualmente, sugerindo a criação de um para containerização (ex.: multi-stage build com nginx).
- **Banco de Dados**: MySQL dockerizado via `docker-compose.yml` (serviço `db`), com healthcheck configurado.

### Pontos Críticos
- O serviço de autenticação no `docker-compose.yml` aponta para `./auth`, mas o diretório correto é `./autenticacao`. Ajuste necessário.
- O frontend não tem Dockerfile; considere adicionar um para consistência com os outros serviços.

## Estrutura do Projeto

```
├───autenticacao            # Serviço de autenticação
│   ├───auth
│   └───config
├───backend                 # API FastAPI
│   ├───config
│   ├───mysql-init
│   └───source
│       ├───episodio
│       ├───gatilho
│       ├───medicacao
│       └───usuario
├───documentacao            # Documentação
│   ├───assets
│   ├───docs
│   ├───logs
│   └───scripts
└───frontend                # Interface React/Vite
    ├───build
    ├───node_modules
    ├───src
    └───tests-selenium
```

### Estrutura da Documentação

/assets → logos, ícones, paleta de cores

/docs → guia de estilo, backlog, regras de negócio, MVP, protótipo de alta fidelidade, diagrama lógico

## Deploy no Railway

### Pré-requisitos
- Conta no [Railway](https://railway.app)
- Projeto GitHub conectado

### Passos para Deploy

1. **Criar projeto no Railway**
   - Conecte seu repositório GitHub
   - Railway detectará automaticamente os serviços

2. **Configurar variáveis de ambiente**

   Para cada serviço, configure as seguintes variáveis:

   #### Auth Service (Autenticação):
   ```
   MYSQL_ROOT_PASSWORD="ignore"
   MYSQL_USER="user"
   MYSQL_PASSWORD="senha"
   MYSQL_DB="defaultdb"
   MYSQL_HOST="mysql-2e80f044-diario-de-enxaqueca.k.aivencloud.com"
   MYSQL_PORT="24445"
   MYSQL_USE_SSL="True"
   MYSQL_SSL_CA="/app/ca.pem"
   SECRET_KEY="senha"
   ALGORITHM="HS256"
   ACCESS_TOKEN_EXPIRE_MINUTES="1440"
   APP_HOST="0.0.0.0"
   APP_PORT="8000"
   AUTH_PORT="8001"
   ENVIRONMENT="production"
   DEBUG="False"
   MAIL_USERNAME="email@mail.com"
   MAIL_PASSWORD="senha"
   MAIL_FROM="email@mail.com"
   MAIL_PORT="587"
   MAIL_SERVER="smtp.mail.com"
   MAIL_STARTTLS="True"
   MAIL_SSL_TLS="False"
   ```

   #### Backend Service:
   ```
   MYSQL_ROOT_PASSWORD="ignore"
   MYSQL_USER="user"
   MYSQL_PASSWORD="senha"
   MYSQL_DB="defaultdb"
   MYSQL_HOST="mysql-2e80f044-diario-de-enxaqueca.k.aivencloud.com"
   MYSQL_PORT="24445"
   MYSQL_USE_SSL="True"
   MYSQL_SSL_CA="/app/ca.pem"
   SECRET_KEY="senha"
   ALGORITHM="HS256"
   ACCESS_TOKEN_EXPIRE_MINUTES="1440"
   APP_HOST="0.0.0.0"
   APP_PORT="8000"
   AUTH_PORT="8001"
   ENVIRONMENT="production"
   DEBUG="False"
   MAIL_USERNAME="email@mail.com"
   MAIL_PASSWORD="senha"
   MAIL_FROM="email@mail.com"
   MAIL_PORT="587"
   MAIL_SERVER="smtp.mail.com"
   MAIL_STARTTLS="True"
   MAIL_SSL_TLS="False"
   ```

   #### Frontend Service:
   ```
   VITE_BACKEND_URL="https://backend-production-f9d7.up.railway.app/api"
   VITE_AUTH_URL="https://autenticacao-production-00f7.up.railway.app/api/auth"
   ```

3. **Configurar domínio (opcional)**
   - Vá para Settings > Domains
   - Adicione seu domínio customizado

4. **Verificar deploy**
   - Acesse a URL do frontend: https://frontend-production-7dfd.up.railway.app
   - Teste login/cadastro
   - Verifique se as APIs estão respondendo:
     - Backend: https://backend-production-f9d7.up.railway.app
     - Auth: https://autenticacao-production-00f7.up.railway.app

## Desenvolvimento Local

### Pré-requisitos
- Docker e Docker Compose
- Node.js 18+ (para desenvolvimento frontend)
- Python 3.11+ (para desenvolvimento backend)

### Executar localmente

```bash
# Clonar repositório
git clone <repository-url>
cd diario-enxaqueca

# Subir todos os serviços
docker compose up --build -d

# Verificar status
docker compose ps

# Ver logs
docker compose logs -f
```

### Endpoints locais
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- Auth Service: http://localhost:8001
- Database: localhost:3306

## Configuração de Ambiente

### Produção vs Desenvolvimento

| Variável | Desenvolvimento | Produção |
|----------|----------------|----------|
| BACKEND_URL | http://backend:8000 | https://backend-production-f9d7.up.railway.app |
| AUTH_URL | http://auth:8001 | https://autenticacao-production-00f7.up.railway.app |


### Arquivos de Configuração
- `.env.local` - Exemplo para desenvolvimento
- `.env.prod` - Configurações de produção

## Testes

```bash
# Testes do backend
docker compose run --rm tests

# Testes do auth
docker compose run --rm tests-auth

# Lint
docker compose run --rm lint
```

## Documentação do Projeto

Consulte a pasta `documentacao/` para:
- Diagrama UML
- Documentação da API
- Guias de usuário

### Conteúdo da documentação

- **[Guia de estilo](./docs/guia-de-estilo.md):** identidade visual (logo, paleta, tipografia, ícones)
- **[Protótipo (Figma)](./docs/prototipo.md):** representação das interfaces conforme o MVP
- **Definição do [MVP](./docs/mvp.md)**
- **[Backlog](./docs/backlog.md):** lista de histórias de usuário (mínimo de 10)
- **[Regras de negócio](./docs/regras-de-negocio.md):** descrição funcional do sistema
- **Diagramas UML:** estrutura ([Diagrama de classes](./docs/diagrama-classes.md)) e comportamento ([Diagrama de sequência](./docs/diagrama-sequencia.md))

## Links

- [Organização principal](https://github.com/diario-enxaqueca)
- [Backend](https://github.com/diario-enxaqueca/backend)
- [Frontend](https://github.com/diario-enxaqueca/frontend)
- [Autenticação](https://github.com/diario-enxaqueca/autenticacao)

## Boas Práticas
- Toda a documentação segue a norma **ABNT NBR 6023:2020** para referências.
- Diagramas feitos com **Draw.io**.
- Protótipos criados com **Figma**.

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

Este projeto está sob a licença MIT.

[MIT License](./LICENSE) © [ZenildaVieira]
