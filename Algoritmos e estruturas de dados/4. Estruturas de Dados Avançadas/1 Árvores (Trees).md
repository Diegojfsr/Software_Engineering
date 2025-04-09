**Árvores** são uma estrutura de dados hierárquica que modela relações entre elementos, organizados de forma semelhante a uma árvore natural, com um **nó raiz** (_root node_) no topo e **nós filhos** (_child nodes_) que se ramificam abaixo. Em informática e algoritmos, árvores são fundamentais para organizar, armazenar e manipular dados de forma eficiente.

### **Estrutura de uma Árvore**

Uma árvore é composta de:

1. **Nó (Node)**:
    - Cada elemento da árvore é chamado de nó.
    - Um nó pode conter dados e referências para outros nós.
2. **Raiz (Root)**:
    - O nó mais alto da árvore, que serve como ponto de partida.
3. **Filhos (Children)**:
    - Nós conectados diretamente a outro nó (nó pai).
4. **Folhas (Leaves)**:
    - Nós que não possuem filhos (nós finais da árvore).
5. **Altura da Árvore**:
    - O número de níveis ou camadas da árvore.

Exemplo visual:

```
         A (raiz)
       /   \
      B     C
     / \   / \
    D   E F   G
```

### **Tipos de Árvores**

Existem diferentes tipos de árvores, dependendo da organização dos nós:

1. **Árvore Binária**:
    - Cada nó pode ter no máximo dois filhos.
2. **Árvore Binária de Busca (BST)**:
    - Uma árvore binária onde os valores menores que o nó estão à esquerda, e os maiores à direita.
3. **Árvore Balanceada**:
    - Uma árvore em que a altura dos nós está equilibrada, minimizando o tempo de busca.
4. **Árvore AVL**:
    - Tipo de BST onde a diferença de altura entre subárvores é no máximo 1.
5. **Árvore B**:
    - Usada em sistemas de banco de dados e armazenamento para indexação eficiente.
6. **Árvore Trie**:
    - Usada para pesquisar texto, armazenando sequências de caracteres.

### **Características e Propriedades**

- **Hierárquica**: Cada nó é conectado de forma que não haja ciclos.
- **Rápida**: Árvores são eficientes para busca, inserção e remoção, dependendo do tipo de árvore.
- **Dinâmica**: Elas podem crescer e se adaptar conforme os dados mudam.

### **Aplicações**

- **Sistemas de Arquivos**: Representar diretórios e arquivos em um computador.
- **Banco de Dados**: Usadas para indexar e organizar informações em operações rápidas.
- **Inteligência Artificial**: Para tomada de decisão em árvores de decisão ou jogos.
- **Pesquisa de Texto**: Árvores Trie são usadas em mecanismos de busca.
- **Grafos**: Muitas vezes, algoritmos em grafos dependem de árvores.


