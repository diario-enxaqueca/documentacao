# Regras de Negócio


### Entradas de Enxaqueca

* Cada `episódio` pertence a um usuário (usuario_id obrigatório).
* A `data do episódio` é obrigatória e não pode ser futura.
* A `intensidade` deve ser um número de 0 a 10.
* Os `gatilhos` podem ser múltiplos, mas não nulos.
* As `medicacoes` podem ser múltiplas, mas podem estar vazias.
* As `observacoes` pode ter no máximo 500 caracteres.
* Usuário só pode criar, editar ou deletar seus próprios episódios.
* Ao criar um episódio, ela deve ser armazenada no banco MySQL.
* Ao listar episódios, devem aparecer ordenadas por data decrescente.
* Ao editar episódio, apenas data, intensidade e descrição podem ser alteradas.
* Deletar `episódio` remove o episódio permanentemente do banco.

### Usuários

* O `email` deve ser único e seguir formato válido.
* A `senha` deve ter mínimo 6 caracteres.
* Usuário só pode editar seus próprios dados.
* Administrador pode editar/deletar qualquer usuário.

### Dashboard / Estatísticas

* Mostrar apenas episódios do usuário logado.
* Os gráficos calculam média de intensidade e frequência por período.
* Filtros podem ser aplicados somente aos episódios visíveis.

### Validações Gerais

* Todos os campos obrigatórios devem ser preenchidos antes do envio.
* Mensagens de erro claras devem ser para usuário.
* Backend retorna códigos HTTP adequados (`200`, `201`, `400`, `404`, `403`)

