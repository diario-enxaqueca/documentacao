# Regras de Negócio


### Entradas de Enxaqueca

* Cada `entrada` pertence a um usuário (usuario_id obrigatório).
* A `data da entrada` é obrigatória e não pode ser futura.
* A `intensidade` deve ser um número de 0 a 10.
* Os `gatilhos` podem ser múltiplos, mas não nulos.
* As `medicacoes` podem ser múltiplas, mas podem estar vazias.
* As `observacoes` pode ter no máximo 500 caracteres.
* Usuário só pode criar, editar ou deletar seus próprios registros.
* Ao criar uma entrada, ela deve ser armazenada no banco MySQL.
* Ao listar entradas, devem aparecer ordenadas por data decrescente.
* Ao editar entrada, apenas data, intensidade e descrição podem ser alteradas.
* Deletar `entrada` remove o registro permanentemente do banco.

### Usuários

* O `email` deve ser único e seguir formato válido.
* A `senha` deve ter mínimo 6 caracteres.
* Usuário só pode editar seus próprios dados.
* Administrador pode editar/deletar qualquer usuário.

### Dashboard / Estatísticas

* Mostrar apenas registros do usuário logado.
* Os gráficos calculam média de intensidade e frequência por período.
* Filtros podem ser aplicados somente aos registros visíveis.

### Validações Gerais

* Todos os campos obrigatórios devem ser preenchidos antes do envio.
* Mensagens de erro claras devem ser para usuário.
* Backend retorna códigos HTTP adequados (`200`, `201`, `400`, `404`, `403`)

