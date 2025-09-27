# MVP – Projeto Completo do Diário de Enxaqueca

### MVP do Projeto Completo

**Recurso principal:** **Entrada de Enxaqueca**

#### Funcionalidades

1. **CRUD de Entradas de Enxaqueca**

   * Criar, listar, visualizar, editar e deletar registros
   * Campos:

     * `data` (data do episódio)
     * `intensidade` (0 a 10)
     * `gatilhos` (lista de gatilhos)
     * `medicacoes` (lista de medicações usadas)
     * `observacoes` (campo de texto livre)

2. **Gestão de Usuários**

   * CRUD de usuários: criar, listar, editar, deletar
   * Campos: `nome`, `email`, `senha`
   * Validações: e-mail único, senha segura

3. **Dashboard de Estatísticas**

   * Gráficos: intensidade média, episódios por mês, gatilhos mais comuns
   * Filtros por período e intensidade

4. **Busca e Filtragem de Registros**

   * Pesquisar por data, intensidade ou gatilho

5. **Configurações do Usuário**

   * Atualização de dados pessoais e preferências
   * Alteração de senha

#### Observações

* Backend MVC, frontend estruturado em páginas/componentes.
* Banco de dados MySQL, dockerizado, com SQLAlchemy.
* Autenticação JWT para usuários (somente quando implementado).
* Documentação completa, protótipo Figma e testes integrados.

