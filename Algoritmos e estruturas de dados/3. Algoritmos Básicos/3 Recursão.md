**Recursão** é uma técnica em programação onde uma função se chama novamente dentro de sua própria definição. Isso permite resolver problemas complexos ao dividi-los em subproblemas menores e mais simples, que podem ser tratados de forma semelhante ao problema original.

### **Como funciona a Recursão?**

1. **Caso Base**: É a condição que encerra a recursão. Sem um caso base, a função continuará chamando a si mesma indefinidamente, levando a um _stack overflow_ (estouro da pilha).
2. **Chamada Recursiva**: É o momento em que a função se chama novamente com uma entrada menor ou simplificada, aproximando-se do caso base.

### **Exemplo Básico: Fatorial**

O cálculo de n!n! (fatorial de nn) é uma aplicação clássica de recursão:
- n!=n×(n−1)!n! = n \times (n-1)!, com o caso base 0!=10! = 1.

**Implementação em Python**:

```
def fatorial(n):
    if n == 0:  # Caso base
        return 1
    return n * fatorial(n - 1)  # Chamada recursiva

# Uso
print(fatorial(5))  # Saída: 120
```

### **Pilha de Recursão**

A recursão utiliza a **pilha de execução** para armazenar as chamadas pendentes da função. Cada vez que uma função é chamada, uma nova instância é adicionada à pilha, e as instâncias são resolvidas na ordem inversa.

**Para fatorial(3):**
1. fatorial(3): 3×fatorial(2)3 \times fatorial(2)
2. fatorial(2): 2×fatorial(1)2 \times fatorial(1)
3. fatorial(1): 1×fatorial(0)1 \times fatorial(0)
4. fatorial(0): Retorna 1 (caso base).
5. Resolve fatorial(1), depois fatorial(2) e finalmente fatorial(3).

### **Vantagens**

- Simplifica a solução de problemas complexos (como árvores, grafos, e problemas de divisão e conquista).
- Código mais limpo e legível para alguns cenários.

### **Desvantagens**

- **Risco de Estouro da Pilha**: Muitas chamadas recursivas podem levar ao esgotamento da memória.
- **Desempenho**: Pode ser mais lento do que soluções iterativas, especialmente sem otimização.
- **Dificuldade de Depuração**: Pode ser mais difícil rastrear erros.

### **Exemplo Prático: Sequência de Fibonacci**

Outro exemplo clássico é calcular o nn-ésimo número de Fibonacci:

- F(n)=F(n−1)+F(n−2)F(n) = F(n-1) + F(n-2), com F(0)=0F(0) = 0 e F(1)=1F(1) = 1.

```
def fibonacci(n):
    if n <= 1:  # Caso base
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)  # Chamada recursiva

# Uso
print(fibonacci(6))  # Saída: 8
```

### **Cuidados com a Recursão**

1. Sempre inclua um caso base para evitar loops infinitos.
2. Use **memoization** (armazenar os resultados das chamadas) para otimizar recursões excessivas, como no cálculo de Fibonacci.
3. Em problemas onde a pilha cresce muito, considere soluções iterativas.

