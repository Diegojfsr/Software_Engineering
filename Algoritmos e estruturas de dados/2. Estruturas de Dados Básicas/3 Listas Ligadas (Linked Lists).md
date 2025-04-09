**Listas Ligadas (Linked Lists)** são uma estrutura de dados linear que armazena uma coleção de elementos chamados "nós" (_nodes_). Diferentemente dos arrays, onde os elementos estão em posições consecutivas na memória, em uma lista ligada, os elementos podem estar espalhados, mas cada nó contém uma referência para o próximo, criando uma cadeia.

### **Como funciona uma Lista Ligada?**

Cada nó de uma lista ligada contém:
1. **Dados**: O valor que aquele nó armazena (por exemplo, um número ou caractere).
2. **Ponteiro (ou referência)**: Um link que aponta para o próximo nó na lista.

Exemplo visual de uma lista ligada simples:

```
[ Dado | Próximo ] -> [ Dado | Próximo ] -> [ Dado | Próximo ] -> None
```

O último nó aponta para `None` (ou `null`), indicando o fim da lista.

### **Tipos de Listas Ligadas**

1. **Lista Simplesmente Ligada (Singly Linked List)**:
    - Cada nó aponta apenas para o próximo nó.
    - Exemplo:

        ```
        [10 | Próximo] -> [20 | Próximo] -> [30 | None]
        ```

2. **Lista Duplamente Ligada (Doubly Linked List)**:
    - Cada nó tem dois ponteiros: um para o próximo e outro para o anterior.
    - Exemplo:

        ```
        None <- [10 | Próx/Ant] <-> [20 | Próx/Ant] <-> [30 | None]
        ```

3. **Lista Circular**:
    - Os nós estão conectados de forma que o último aponta para o primeiro, formando um ciclo.
    - Exemplo:

        ```
        [10 | Próximo] -> [20 | Próximo] -> [30 | Próximo] -> [10 | Próximo]
        ```

### **Vantagens das Listas Ligadas**

- Inserções e remoções são mais eficientes do que em arrays, especialmente no início ou meio da lista (**O(1)** no melhor caso, contra **O(n)** em arrays).
- Seu tamanho pode crescer dinamicamente sem a necessidade de realocação de memória, diferente dos arrays.

### **Desvantagens**

- Acesso aos elementos é mais lento (**O(n)** para busca), já que é necessário percorrer os nós um por um.
- Consome mais memória devido aos ponteiros extras em cada nó.

### **Aplicações**

- Implementação de filas (_queues_) e pilhas (_stacks_).
- Manipulação de grandes coleções de dados que mudam frequentemente (como inserções e exclusões).
- Criar tabelas hash, onde buckets podem ser listas ligadas.

