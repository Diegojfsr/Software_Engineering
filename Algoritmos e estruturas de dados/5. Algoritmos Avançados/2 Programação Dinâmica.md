**Programação Dinâmica (Dynamic Programming)** é uma técnica de programação usada para resolver problemas complexos ao dividi-los em subproblemas menores e mais simples. A ideia principal é resolver cada subproblema **uma única vez** e armazenar o resultado (em memória ou em uma tabela), evitando calcular novamente.

Essa abordagem é amplamente aplicada em problemas de **otimização** e **combinatória**, onde o mesmo subproblema se repete várias vezes.

### **Princípios Fundamentais**

A Programação Dinâmica funciona com base em dois princípios principais:
1. **Subproblemas sobrepostos**:
    - Muitos problemas possuem subproblemas que se repetem várias vezes durante a execução.
    - Exemplo: Na sequência de Fibonacci, para calcular F(5)F(5), é necessário calcular F(4)F(4) e F(3)F(3), e esses mesmos cálculos aparecem quando F(4)F(4) é computado.
2. **Subestrutura ótima**:
    - A solução ótima do problema pode ser construída a partir das soluções ótimas de seus subproblemas.
    - Exemplo: Na mochila de peso máximo (**Knapsack Problem**), a melhor solução para um conjunto de itens inclui as melhores soluções para subgrupos menores desses itens.

### **Como Resolver Problemas com Programação Dinâmica**

1. **Definir o Problema Recursivamente**:
    - Quebrar o problema principal em subproblemas menores e identificar as relações entre eles.
2. **Armazenar Resultados (Memoization ou Tabulação)**:
    - Usar uma técnica para salvar os resultados dos subproblemas:
        - **Memoization**: Salva os resultados em uma estrutura como um dicionário ou array enquanto calcula os subproblemas recursivamente.
        - **Tabulação**: Preenche uma tabela iterativamente começando com os casos base.
3. **Determinar os Casos Base**:
    - Os casos triviais que resolvem o problema sem precisar de recursão ou cálculos adicionais.

### **Exemplo Clássico: Sequência de Fibonacci**

A sequência de Fibonacci é definida por:

- F(0)=0,F(1)=1F(0) = 0, F(1) = 1
- F(n)=F(n−1)+F(n−2)F(n) = F(n-1) + F(n-2) para n>1n > 1

#### **Implementação com Programação Dinâmica**

##### **Memoization**:

```
def fibonacci(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fibonacci(n-1, memo) + fibonacci(n-2, memo)
    return memo[n]

# Uso
print(fibonacci(10))  # Saída: 55
```

##### **Tabulação**:

```
def fibonacci_tab(n):
    tabela = [0, 1]
    for i in range(2, n+1):
        tabela.append(tabela[i-1] + tabela[i-2])
    return tabela[n]

# Uso
print(fibonacci_tab(10))  # Saída: 55
```

### **Exemplo de Problema: Mochila (Knapsack Problem)**

Dado um conjunto de itens com pesos e valores, e uma mochila com capacidade máxima, encontre o valor máximo que pode ser carregado.

#### **Abordagem com DP**:

1. Definir uma tabela onde cada entrada representa o valor máximo para um determinado peso.
2. Resolver iterativamente, considerando incluir ou não cada item.

```
def knapsack(valores, pesos, capacidade):
    n = len(valores)
    tabela = [[0 for _ in range(capacidade + 1)] for _ in range(n + 1)]

    for i in range(1, n + 1):
        for w in range(1, capacidade + 1):
            if pesos[i-1] <= w:
                tabela[i][w] = max(valores[i-1] + tabela[i-1][w-pesos[i-1]], tabela[i-1][w])
            else:
                tabela[i][w] = tabela[i-1][w]

    return tabela[n][capacidade]

# Exemplo de uso
valores = [60, 100, 120]
pesos = [10, 20, 30]
capacidade = 50
print(knapsack(valores, pesos, capacidade))  # Saída: 220
```

### **Vantagens**

1. **Eficiência**:
    - Evita cálculos repetidos e melhora o desempenho em problemas com subproblemas sobrepostos.
    - A complexidade pode ser reduzida de **exponencial** para **polinomial**.
2. **Flexibilidade**:
    - Pode ser aplicada em uma ampla gama de problemas, como:
        - Sequências (Fibonacci, Longest Common Subsequence).
        - Grafos (caminhos mais curtos, Floyd-Warshall).
        - Otimização (Knapsack Problem, Cutting Rod).

### **Desvantagens**

1. **Consumo de Memória**:
    - Armazenar os resultados pode demandar grande espaço para tabelas ou estruturas de armazenamento.
2. **Planejamento Complexo**:
    - Exige conhecimento profundo do problema e habilidade de modelá-lo em termos de subproblemas.
