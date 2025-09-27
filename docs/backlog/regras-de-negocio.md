# 3. Regras de Negócio


### Entradas de Enxaqueca

* `data` não pode ser futura
* `intensidade` deve estar entre 0 e 10
* `gatilhos` podem ser múltiplos, mas não nulos
* `medicacoes` podem ser múltiplas, mas podem estar vazias
* `observacoes` máximo de 500 caracteres
* Usuário só pode criar, editar ou deletar seus próprios registros

### Usuários

* `email` deve ser único
* `senha` deve ter mínimo 6 caracteres
* E-mail deve seguir formato válido
* Usuário só pode editar seus próprios dados
* Administrador pode editar/deletar qualquer usuário

### Dashboard / Estatísticas

* Mostrar apenas registros do usuário logado
* Gráficos calculam média de intensidade e frequência por período
* Filtros aplicam somente aos registros visíveis

### Validações Gerais

* Todos os campos obrigatórios devem ser preenchidos antes do envio
* Mensagens de erro claras para usuário
* Backend retorna códigos HTTP adequados (`200`, `201`, `400`, `404`, `403`)

