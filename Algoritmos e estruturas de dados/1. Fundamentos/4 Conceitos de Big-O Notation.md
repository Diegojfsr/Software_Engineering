A _Big-O Notation_ é uma forma de descrever a eficiência de algoritmos, especialmente em termos de **tempo de execução** e **uso de memória** à medida que o tamanho da entrada (_n_) cresce. Ela foca no comportamento de desempenho no pior caso ou no crescimento assintótico. Aqui estão os conceitos principais:

### **1. Crescimento Assintótico**

A _Big-O Notation_ se concentra em como o desempenho do algoritmo escala conforme _n_ aumenta, ignorando constantes e termos menores. É como olhar para "o que mais importa" em entradas muito grandes.

### **2. Tipos Comuns de Complexidade**

Cada tipo de _Big-O_ representa um padrão de crescimento. Aqui estão os mais frequentes:

- **O(1) - Constante**: O desempenho não depende do tamanho da entrada. Exemplo: acessar diretamente um elemento em um array.
- **O(log n) - Logarítmico**: Aumenta lentamente com o tamanho da entrada. Exemplo: busca binária.
- **O(n) - Linear**: O tempo cresce proporcionalmente ao tamanho da entrada. Exemplo: percorrer todos os elementos de uma lista.
- **O(n log n) - Linearítmico**: Comum em algoritmos de ordenação eficientes como _Merge Sort_.
- **O(n²) - Quadrático**: Cresce rapidamente. Exemplo: algoritmos de ordenação mais simples, como _Bubble Sort_.
- **O(2ⁿ) - Exponencial**: Muito ineficiente, pois o crescimento é exponencial. Exemplo: resolver o problema da mochila (_Knapsack_) de forma ingênua.
- **O(n!) - Fatorial**: Raramente viável para problemas maiores. Exemplo: analisar todas as permutações possíveis.

### **3. Pior Caso, Caso Médio e Melhor Caso**

- **Pior Caso** (_Worst Case_): Cenário em que o algoritmo tem seu pior desempenho.
- **Caso Médio** (_Average Case_): Desempenho em situações típicas.
- **Melhor Caso** (_Best Case_): Cenário mais otimista, mas geralmente pouco útil na prática.

### **4. Comparação de Desempenho**

A _Big-O Notation_ ajuda a comparar diferentes algoritmos para escolher o mais eficiente. Por exemplo, um algoritmo de ordenação _O(n log n)_ será muito mais rápido que um _O(n²)_ para entradas grandes.

### **5. Ignorar Constantes**

Na análise de _Big-O_, os fatores constantes são ignorados porque não afetam o crescimento para grandes entradas. Por exemplo:
- Se um algoritmo leva 5n+105n + 10 passos, seu _Big-O_ seria simplificado para O(n)O(n).


