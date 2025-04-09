**Hash Tables** (ou **Mapas**, em alguns contextos) são uma estrutura de dados altamente eficiente que armazena pares de **chave-valor** e permite acesso rápido aos dados. Essa rapidez é alcançada por meio de uma função chamada **função hash**, que converte a chave em um índice em um array subjacente.

### **Como funcionam as Hash Tables**

1. **Chave-Valor**: Cada dado armazenado tem uma **chave única** (como um identificador) e um **valor** associado.
    - Exemplo: "nome" é a chave, e "Diego" é o valor.
2. **Função Hash**: A chave é processada por uma função hash, que calcula um índice no array onde o valor será armazenado.
    - Exemplo:

        ```
        chave = "nome" -> função hash -> índice = 3
        ```

        O valor "Diego" é armazenado na posição 3.

3. **Acesso Rápido**: Para acessar um valor, a chave é novamente passada pela função hash para localizar o índice rapidamente.

### **Vantagens**

1. **Rápido acesso aos dados**:
    - Em casos ideais, permite acesso, inserção e remoção em tempo **O(1)** (constante).
2. **Flexível**:
    - Permite armazenar e acessar grandes volumes de dados, desde que as chaves sejam bem distribuídas pela função hash.

### **Problemas e Soluções**

1. **Colisões**: Quando duas chaves diferentes produzem o mesmo índice, ocorre uma colisão.
    - **Soluções**:
        - **Encadeamento**: Os valores que colidem são armazenados em uma lista ligada no mesmo índice.
        - **Probing**: Procura outro espaço no array para armazenar o valor.
2. **Custo de Rehashing**: Quando a tabela cresce muito, é necessário redimensioná-la, o que pode ser um processo caro.

### **Exemplo em Python com um Dicionário**

Em Python, os dicionários são implementados como hash tables. Aqui está um exemplo:

```
# Criando um dicionário (hash table)
hash_table = {"nome": "Diego", "idade": 25, "cidade": "Miradouro"}

# Acessando valores
print(hash_table["nome"])  # Saída: Diego

# Adicionando e removendo valores
hash_table["profissão"] = "Engenheiro"
del hash_table["idade"]

print(hash_table)  # Saída: {'nome': 'Diego', 'cidade': 'Miradouro', 'profissão': 'Engenheiro'}
```

### **Aplicações das Hash Tables**

- **Cache de Dados**: Recuperar informações rapidamente.
- **Tabelas de Simbolos**: Usadas por compiladores para armazenar variáveis e funções.
- **Banco de Dados e Indexação**: Para acesso rápido a registros.
- **Detecção de Duplicados**: Armazenar elementos únicos para verificar duplicatas.


