Os **bancos de dados relacionais** (RDB - Relational Database) são um tipo de banco de dados que organiza informações em **tabelas**. Essas tabelas são compostas por linhas e colunas, e os dados são estruturados de forma que possam ser relacionados uns aos outros. Eles são baseados no modelo relacional, criado por **Edgar F. Codd** em 1970, e utilizam **Structured Query Language (SQL)** para manipulação e consulta de dados.

### **Características principais:**

1. **Estrutura em tabelas:**
    - Os dados são armazenados em tabelas organizadas em **linhas** (registros) e **colunas** (campos).
    - Cada linha representa um registro único, enquanto as colunas representam os atributos do registro.
2. **Relacionamentos entre tabelas:**
    - As tabelas podem ser relacionadas entre si por meio de **chaves primárias** e **chaves estrangeiras**.
    - Isso permite criar conexões entre dados de diferentes tabelas, garantindo consistência.
3. **Uso de SQL:**
    - SQL é utilizado para criar, manipular e consultar os dados armazenados no banco.
    - Exemplos: `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
4. **Integridade dos dados:**
    - Garantem consistência e validação por meio de regras como restrições de chave primária, unicidade, e integridade referencial.

### **Exemplo prático**

Imagine um sistema de gestão de uma livraria:

- **Tabela Livros:** Contém informações como `ID_Livro`, `Título`, `Autor`, `Preço`.
- **Tabela Clientes:** Contém dados como `ID_Cliente`, `Nome`, `Email`.
- **Tabela Pedidos:** Relaciona os clientes aos livros comprados (`ID_Cliente` e `ID_Livro` são chaves estrangeiras).

**Relacionamento:** Um cliente pode fazer vários pedidos, e cada pedido pode conter vários livros.

### **Vantagens:**

- **Organização:** Estrutura clara e intuitiva baseada em tabelas.
- **Consistência:** Relações entre tabelas garantem dados precisos e integrados.
- **Flexibilidade:** SQL oferece ferramentas poderosas para consultar e manipular os dados.
- **Ampla adoção:** Muitas empresas e sistemas utilizam bancos de dados relacionais (ex.: MySQL, PostgreSQL, Oracle Database, SQL Server).

### **Desvantagens:**

- **Escalabilidade limitada:** Em sistemas que precisam armazenar grandes volumes de dados não estruturados, podem enfrentar dificuldades.
- **Complexidade em grandes relacionamentos:** Muitos relacionamentos entre tabelas podem tornar o gerenciamento mais complexo.


