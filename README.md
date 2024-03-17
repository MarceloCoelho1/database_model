# Modelo Entidade-Relacionamento para Biblioteca

Este documento descreve o modelo entidade-relacionamento (MER) para um sistema de gerenciamento de biblioteca. O sistema é composto por entidades fortes e fracas, relacionamentos e atributos específicos para cada setor da biblioteca.

## Entidades e Relacionamentos

### Entidades Fortes

- **Biblioteca**: Entidade central do sistema.
- **Fornecedor**: Responsável por fornecer novos livros.
- **Novo usuário**: Um novo usuário.
- **Usuário**: Usuário já cadastrado no sistema.


### Entidades Fracas

- **ADM**: É responsável pelo gerenciamento em geral da biblioteca, no modelo essa entidade fica responsável pela solicitação de novos livros dos fornecedores (foi omitido o fato de cuidar do gerenciamento geral da biblioteca)
- **Gerenciamento de Usuários**: Gerencia o cadastro de usuario e armazena os dados no banco de dados.
- **Circulação de Materiais**: Gerencia toda a circulação de materiais seja um emprestimo, devolução, multa, alocação dos livros em plataformas etc.


### Relacionamentos

- **Usuário - Empréstimo**: Um usuário pode fazer até 6 empréstimos simultâneos.
- **Usuário - Lista de Espera**: Usuários são adicionados a uma lista de espera para solicitar livros.
- **ADM - Fornecedor**: O setor ADM pode solicitar novos livros dos fornecedores.
- **NOVO USUARIO - Cadastro na biblioteca**: Responsável por cadastrar novos usuários.

## Especializações de Usuários

- **Funcionário**: Usuários com prioridade no empréstimo de livros.
- **Usuário Comum**: Usuários sem prioridade.

## Setores e Subsetores

### ADM

- **Responsabilidades**: Pedidos de livros para fornecedores, administração geral da biblioteca.

### Circulação de Materiais

- **Responsabilidades**: Movimentações de livros (empréstimo, devolução, alocação), multas.
- **Subsetor de Multas**: Registro de multas dos usuários.

### Gerencia Usuários

- **Responsabilidades**: Responsável por guardar as informações de usuários cadastrados e cadastrar novos usuários.
