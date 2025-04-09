**Heaps** são uma estrutura de dados especial que segue uma propriedade fundamental chamada **propriedade de heap**. Eles são geralmente representados como árvores binárias completas (ou quase completas), onde cada nível da árvore é preenchido da esquerda para a direita, exceto, possivelmente, o último nível. Os heaps são amplamente usados em algoritmos eficientes, como em filas de prioridade e ordenação de dados.

### **Tipos de Heaps**

1. **Max-Heap**:
    - A propriedade do **Max-Heap** garante que o valor de qualquer nó seja **maior ou igual aos valores de seus filhos**.
    - O maior valor está sempre no nó raiz.
2. **Min-Heap**:
    - A propriedade do **Min-Heap** garante que o valor de qualquer nó seja **menor ou igual aos valores de seus filhos**.
    - O menor valor está sempre no nó raiz.

### **Representação de um Heap**

Embora os heaps sejam visualmente representados como árvores binárias, eles são comumente armazenados em **arrays** para simplificar a manipulação.

**Exemplo de Max-Heap**:

```
       50
      /  \
    30    20
   / \    / \
  10 15  8   5
```

**Array correspondente**: `[50, 30, 20, 10, 15, 8, 5]`

### **Operações em Heaps**

1. **Inserção**:
    - Adiciona o novo elemento no final do heap (posição mais à direita no array).
    - Realiza um processo chamado **"heapify-up"** ou **ajuste para cima**, para garantir que a propriedade do heap seja mantida.
2. **Remoção (Extração do Elemento Raiz)**:
    - Remove o elemento no topo (raiz), que é o maior (em Max-Heap) ou o menor (em Min-Heap).
    - Substitui o topo pelo último elemento no heap.
    - Realiza o **"heapify-down"** ou **ajuste para baixo**, para restaurar a propriedade do heap.
3. **Construção do Heap**:
    - Dado um array não estruturado, converte-o em um heap válido utilizando repetidos ajustes para baixo.

### **Complexidade**

- **Inserção:** O(log⁡n)O(\log n), pois, no pior caso, é necessário subir toda a altura da árvore.
- **Remoção:** O(log⁡n)O(\log n), devido ao processo de ajuste para baixo.
- **Construção:** O(n)O(n), com um método otimizado.
- **Busca pelo Maior ou Menor Elemento:** O(1)O(1), pois eles estão sempre na raiz.

### **Aplicações de Heaps**

1. **Fila de Prioridade**:
    - Implementa uma fila onde os elementos de maior ou menor prioridade são acessados primeiro.
    - Exemplo: Gerenciamento de tarefas em sistemas operacionais.
2. **Heap Sort**:
    - Um algoritmo de ordenação baseado em heaps que utiliza repetidamente a extração do maior/menor elemento.
    - Complexidade: O(nlog⁡n)O(n \log n).
3. **Caminhos Mais Curtos (Dijkstra)**:
    - Utiliza heaps para encontrar caminhos mínimos em grafos ponderados.
4. **Medições Dinâmicas**:
    - Usado para calcular a mediana em fluxos de dados.

### **Exemplo de Código (Python)**

Aqui está um exemplo básico de um Min-Heap:

```
import heapq

# Criando um heap vazio
heap = []

# Inserindo elementos (push)
heapq.heappush(heap, 10)
heapq.heappush(heap, 20)
heapq.heappush(heap, 5)

# Extraindo o menor elemento (pop)
menor = heapq.heappop(heap)
print("Menor elemento:", menor)

# Saída: Menor elemento: 5
print("Estado do heap:", heap)  # Saída: [10, 20]
```

