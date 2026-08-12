# Resumo de Comandos SQL

Este guia fornece uma visÃ£o geral detalhada dos diferentes tipos de comandos SQL, organizados por suas categorias.

## 1. DDL (Data Definition Language - Linguagem de DefiniÃ§Ã£o de Dados)

A DDL Ã© usada para definir ou modificar a estrutura do banco de dados e de seus objetos (como tabelas). Ã‰ como criar o "esqueleto" ou a planta estrutural do seu banco de dados.

### Comandos Principais:

*   **`CREATE`**: Cria novos objetos (como bancos de dados ou tabelas) do zero.
    *   *Exemplo (Banco de Dados)*: `CREATE DATABASE Sales;`
    *   *Exemplo (Tabela)*: 
        ```sql
        CREATE TABLE Products (
          ProductID INT,
          ProductName VARCHAR(100),
          Price DECIMAL
        );
        ```
*   **`ALTER`**: Modifica a estrutura de um objeto existente, como adicionar ou remover colunas em uma tabela, sem a necessidade de excluÃ­-la.
    *   *Exemplo (Adicionar Coluna)*:
        ```sql
        ALTER TABLE Products ADD Category VARCHAR(50);
        ```
    *   *Exemplo (Remover Coluna)*:
        ```sql
        ALTER TABLE Products DROP COLUMN Price;
        ```
*   **`DROP`**: Deleta permanentemente um objeto e todos os seus dados.
    *   *Exemplo*: `DROP TABLE Products;`

### Tabela Resumo DDL

| Comando | AÃ§Ã£o | Objeto Afetado |
| :--- | :--- | :--- |
| **CREATE** | Construir novo | Banco de Dados, Tabela, Schema |
| **ALTER** | Modificar existente | Colunas, Tipos de Dados |
| **DROP** | Excluir | Banco de Dados, Tabela, Schema |

---

## 2. DQL (Data Query Language - Linguagem de Consulta de Dados)

A DQL Ã© usada para recuperar dados do banco de dados.

*   **`SELECT`**: Ã‰ o comando principal e essencial para buscar e recuperar informaÃ§Ãµes contidas nas tabelas.

---

## 3. DML (Data Manipulation Language - Linguagem de ManipulaÃ§Ã£o de Dados)

A DML Ã© responsÃ¡vel por gerenciar os dados em si dentro das tabelas criadas.

*   **`INSERT`**: Adiciona novos registros (linhas) em uma tabela.
*   **`UPDATE`**: Modifica registros jÃ¡ existentes.
*   **`DELETE`**: Remove registros de uma tabela.

---

## 4. DCL (Data Control Language - Linguagem de Controle de Dados)

A DCL Ã© utilizada para gerenciar as permissÃµes e o controle de acesso ao banco de dados.

*   **`GRANT`**: Concede privilÃ©gios de acesso aos usuÃ¡rios.
*   **`REVOKE`**: Revoga ou retira os privilÃ©gios concedidos anteriormente.

---

## 5. TCL (Transaction Control Language - Linguagem de Controle de TransaÃ§Ãµes)

A TCL Ã© empregada para gerenciar as transaÃ§Ãµes que ocorrem no banco de dados, garantindo a integridade dos dados.

*   **`COMMIT`**: Salva permanentemente as mudanÃ§as feitas durante uma transaÃ§Ã£o.
*   **`ROLLBACK`**: Desfaz as mudanÃ§as de uma transaÃ§Ã£o caso ocorra algum erro antes do *commit*.
*   **`SAVEPOINT`**: Define um ponto especÃ­fico dentro de uma transaÃ§Ã£o para o qual Ã© possÃ­vel realizar um *rollback* parcial, sem desfazer a transaÃ§Ã£o inteira.
