Medir a eficiência de algoritmos envolve avaliar **como eles se comportam** em termos de tempo de execução e uso de memória, especialmente conforme o tamanho da entrada cresce. Aqui estão os passos e técnicas principais:

### **1. Avaliação de Complexidade**

A eficiência é analisada usando a **Complexidade de Tempo** e a **Complexidade de Espaço**, geralmente expressas na notação Big-O:

- **Tempo de execução:** Mede quanto tempo o algoritmo leva para completar.
- **Uso de memória:** Analisa quanta memória o algoritmo consome enquanto executa.

### **2. Experimentação com Entradas**

Teste o algoritmo com diferentes tamanhos de entrada (_n_) e registre:

- O tempo que leva para executar (usando ferramentas de medição de tempo, como `System.nanoTime()` em Java).
- O consumo de memória durante a execução.

Exemplo: Executar o algoritmo com entradas de 10, 100, 1000 elementos e observar como o desempenho muda.

### **3. Análise Teórica**

Além dos testes práticos, faça uma análise teórica:
- Identifique os loops e operações principais para determinar o crescimento assintótico.
- Exemplo: Um algoritmo com dois loops aninhados geralmente tem uma complexidade **O(n²)**.

### **4. Uso de Ferramentas de Profiling**

Utilize ferramentas específicas para medir desempenho:

- **Linguagem de programação:** Ferramentas como o Profiler em Python ou o Visual Studio Profiler para C#.
- **Sistemas de monitoramento:** Identifique gargalos no código e operações mais demoradas.

### **5. Comparação entre Algoritmos**

Compare diferentes algoritmos para resolver o mesmo problema. Por exemplo, ao ordenar uma lista:
- **Bubble Sort (O(n²))** será muito mais lento que **Quick Sort (O(n log n))** para grandes entradas.

### **6. Testes para Cenários Diferentes**

Analise o algoritmo em:
- **Melhor caso:** Quando a entrada já está parcialmente resolvida.
- **Pior caso:** Quando a entrada está no estado menos favorável.
- **Caso médio:** Cenário mais comum.

### **Exemplo Prático**

Vamos medir a eficiência de um algoritmo simples de busca linear:
- Entrada: Lista de números de tamanhos diferentes.
- Processo: Registrar o tempo para encontrar um número.
- Resultado: Confirmar que o tempo cresce proporcionalmente ao tamanho da lista (**O(n)**).


