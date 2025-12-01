# Ponto de Controle 1

* Diagrama DDL e script SQL
  * [Diagrama Lógico](https://github.com/diario-enxaqueca/documentacao/blob/main/docs/diagrama-logico.md)
* Backlog
  * [Backlog](https://github.com/diario-enxaqueca/documentacao/blob/main/docs/backlog.md)
* Protótipo de Alta Fidelidade
  * [Protótipo](https://github.com/diario-enxaqueca/documentacao/blob/main/docs/prototipo.md)
* Docker
  * [docker-compose.yml](https://github.com/diario-enxaqueca/desenv/blob/main/docker-compose.yml)
  * [Dockerfile - autenticacao](https://github.com/diario-enxaqueca/autenticacao/blob/main/Dockerfile)
  * [Dockerfile - backend](https://github.com/diario-enxaqueca/backend/blob/main/Dockerfile)
  * [Dockerfile - frontend](https://github.com/diario-enxaqueca/frontend/blob/main/Dockerfile)

# Ponto de Controle 2

* Arquitetura
  * [README.md/Arquitetura](https://github.com/diario-enxaqueca/documentacao/blob/main/README.md#arquitetura-do-projeto)  
  
* Clean Code
  * [README.md/Estrutura do Projeto](https://github.com/diario-enxaqueca/documentacao/blob/main/README.md#estrutura-do-projeto)

* Testes Parametrizados
  * Backend
    * [backend/conftest.py](https://github.com/diario-enxaqueca/backend/blob/main/conftest.py)
    * [backend/source/episodio/test_episodio.py](https://github.com/diario-enxaqueca/backend/blob/main/source/episodio/test_episodio.py)
    * [backend/source/gatilho/test_gatilho.py](https://github.com/diario-enxaqueca/backend/blob/main/source/gatilho/test_gatilho.py)
    * [backend/source/medicacao/test_medicacao.py](https://github.com/diario-enxaqueca/backend/blob/main/source/medicacao/test_medicacao.py)
    * [backend/source/usuario/test_usuario.py](https://github.com/diario-enxaqueca/backend/blob/main/source/usuario/test_usuario.py)
  * Autenticação
    * [autenticacao/conftest.py](https://github.com/diario-enxaqueca/autenticacao/blob/main/conftest.py)
    * [autenticacao/auth/test_auth.py](https://github.com/diario-enxaqueca/autenticacao/blob/main/auth/test_auth.py)
  
* Testes de Integração
  * Backend
    * [backend/conftest.py](https://github.com/diario-enxaqueca/backend/blob/main/conftest.py)
    * [backend/source/episodio/test_integration_episodio.py](https://github.com/diario-enxaqueca/backend/blob/main/source/episodio/test_integration_episodio.py)
    * [backend/source/gatilho/test_integration_gatilho.py](https://github.com/diario-enxaqueca/backend/blob/main/source/gatilho/test_integration_gatilho.py)
    * [backend/source/medicacao/test_integration_medicacao.py](https://github.com/diario-enxaqueca/backend/blob/main/source/medicacao/test_integration_medicacao.py)
    * [backend/source/usuario/test_integration_usuario.py](https://github.com/diario-enxaqueca/backend/blob/main/source/usuario/test_integration_usuario.py)
  * Autenticação
    * [autenticacao/conftest.py](https://github.com/diario-enxaqueca/autenticacao/blob/main/conftest.py)
    * [autenticacao/auth/test_integration_auth.py](https://github.com/diario-enxaqueca/autenticacao/blob/main/auth/test_integration_auth.py)

* Banco de Dados
  * [backend/mysql-init/init.sql](https://github.com/diario-enxaqueca/backend/tree/main/mysql-init/init.sql)
  
* Modelo Físico do Banco
  * [Diagrama físico](https://github.com/diario-enxaqueca/backend/blob/main/mysql-init/init.sql)
  
* API em repositório separado
  * [repositório autenticacao](https://github.com/diario-enxaqueca/autenticacao/tree/main) 
  * [repositório backend](https://github.com/diario-enxaqueca/backend/tree/main)
  
* Lint ou derivados - 
  * [lint service - docker-compose.yml](https://github.com/diario-enxaqueca/desenv/blob/main/docker-compose.yml#L101)
  * [lint log](https://github.com/diario-enxaqueca/documentacao/blob/main/registro-logs/lint.log)

# Ponto de Controle 3

* Front completo
  * [Diário de enxaqueca - localhost](http://localhost:3000)

* Hospedagem
  * [Diário de enxaqueca App](https://frontend-production-7dfd.up.railway.app)
  * [autenticacao](https://railway.com/project/158cc4c3-860e-4700-8b9d-c8a4019bbb97/service/f15b020d-c66d-4d29-b53d-7752597855e9?environmentId=e9d28aa0-7bb7-430f-a6ba-a5349d4f8dec&id=90b7d6f8-2d35-4818-95c5-c97cbc740dbe#deploy)
  * [backend](https://railway.com/project/18de0676-54c3-47f5-9dd4-6a8f9a30bd71/service/e3eb481e-c4f8-4823-8edf-6c518ae6445f?environmentId=1101000d-5883-45f0-9cf9-00d42d794353)
  * [frontend](https://railway.com/project/99e1214d-1c16-4970-80d5-2806b6ebed3e/service/05a3f313-f2dd-4e4f-8dda-68e6df6f4942?environmentId=5366094d-4890-46f2-bccb-bac21c5a7f42&id=63a2a5af-d974-41fb-9144-fe18d75632fe#deploy)
  * [Banco de dados MySQL](https://console.aiven.io/account/a5772b2f41a6/project/diario-de-enxaqueca/services)
  
* Testes automatizados com selenium ou afins - 
  * [frontend/tests-selenium/test_diariodeenxaquecaCRUDepisodio.py](https://github.com/diario-enxaqueca/frontend/blob/main/tests-selenium/test_diariodeenxaquecaCRUDepisodio.py)
  * [frontend/tests-selenium/test_diariodeenxaquecaCRUDgatilho.py](https://github.com/diario-enxaqueca/frontend/blob/main/tests-selenium/test_diariodeenxaquecaCRUDgatilho.py)
  * [frontend/tests-selenium/test_diariodeenxaquecaCRUDmedicacao.py](https://github.com/diario-enxaqueca/frontend/blob/main/tests-selenium/test_diariodeenxaquecaCRUDmedicacao.py)
  * [frontend/tests-selenium/test_diariodeenxaquecaCRUDusuario.py](https://github.com/diario-enxaqueca/frontend/blob/main/tests-selenium/test_diariodeenxaquecaCRUDusuario.py)
  * [frontend/tests-selenium/test_diariodeenxaquecaloginlogout.py](https://github.com/diario-enxaqueca/frontend/blob/main/tests-selenium/test_diariodeenxaquecaloginlogout.py)
