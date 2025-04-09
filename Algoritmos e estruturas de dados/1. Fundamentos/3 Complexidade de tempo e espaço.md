A complexidade de tempo e espaço é usada para medir a eficiência de algoritmos em termos de desempenho e uso de recursos. Vamos entender cada uma:

### **Complexidade de Tempo**

Refere-se ao tempo que um algoritmo leva para executar, dependendo do tamanho da entrada (geralmente representado como _n_). Ela é expressa com notação Big-O, que descreve o comportamento no pior caso.

Exemplos:
- **O(1)**: Tempo constante – o tempo de execução não depende do tamanho da entrada.
- **O(n)**: Tempo linear – aumenta proporcionalmente ao tamanho da entrada.
- **O(n²)**: Tempo quadrático – mais lento, como nos algoritmos de ordenação por seleção (_Selection Sort_).
- **O(log n)**: Tempo logarítmico – muito eficiente para entradas grandes, como na busca binária.

### **Complexidade de Espaço**

Refere-se à quantidade de memória necessária para executar o algoritmo, incluindo variáveis, estrutura de dados e chamadas recursivas. Assim como no tempo, é descrita com notação Big-O.

Exemplos:
- **O(1)**: Espaço constante – o algoritmo usa sempre a mesma quantidade de memória, independentemente do tamanho da entrada.
- **O(n)**: Espaço linear – o uso de memória aumenta proporcionalmente ao tamanho da entrada, como armazenar elementos em um array.
- **O(n²)**: Espaço quadrático – menos eficiente, com algoritmos que exigem matrizes ou tabelas grandes.

### Como elas se relacionam:

Algoritmos podem ser otimizados para tempo ou espaço, mas há um equilíbrio a ser alcançado. Por exemplo, ao melhorar a velocidade, um algoritmo pode consumir mais memória, e vice-versa.


