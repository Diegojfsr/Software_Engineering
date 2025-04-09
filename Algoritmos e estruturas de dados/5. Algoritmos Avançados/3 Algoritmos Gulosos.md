**Algoritmos Gulosos** (_Greedy Algorithms_) são uma abordagem de solução de problemas em que decisões locais ótimas são tomadas em cada etapa, na esperança de que essas decisões levem à solução global ótima. Esses algoritmos não revisitam escolhas anteriores, pois assumem que uma solução parcial ótima resultará em uma solução total ótima.

### **Como funcionam os algoritmos gulosos**

1. **Seleção de decisão**:
    - Em cada passo, escolhe-se o melhor elemento disponível com base em um critério específico, sem considerar implicações futuras.
2. **Irrevogabilidade**:
    - As decisões feitas em cada etapa não podem ser alteradas, mesmo se forem subótimas para o conjunto global.
3. **Solução final**:
    - O processo continua até que todos os subproblemas sejam resolvidos ou a solução geral seja construída.

### **Propriedades necessárias**

Para que um algoritmo guloso funcione corretamente, o problema precisa ter:

1. **Propriedade de subestrutura ótima**:
    - Uma solução ótima para o problema pode ser construída a partir de soluções ótimas para seus subproblemas.
    - Exemplo: No problema da mochila fracionária, carregar itens com maior razão valor/peso leva ao resultado global ideal.
2. **Propriedade de escolha gulosa**:
    - Uma escolha feita localmente, com base no critério guloso, deve levar a uma solução global ótima.

Nem todos os problemas possuem essas propriedades, por isso os algoritmos gulosos não funcionam para todos os cenários.

### **Exemplos clássicos de algoritmos gulosos**

1. **Problema da Mochila Fracionária**:
    - Objetivo: Maximizar o valor dos itens carregados na mochila, considerando que pode-se carregar frações dos itens.
    - Abordagem: Selecionar itens com maior razão valor/peso primeiro.
2. **Problema de Huffman**:
    - Objetivo: Criar códigos binários compactos para caracteres com base em sua frequência.
    - Abordagem: Constrói uma árvore usando os dois menores valores de frequência repetidamente.
3. **Problema da Árvore Geradora Mínima**:
    - Objetivo: Conectar todos os vértices de um grafo com o menor custo total.
    - Abordagem: Usar o **algoritmo de Prim** ou **algoritmo de Kruskal** para adicionar arestas de menor peso, evitando ciclos.
4. **Problema do Troco**:
    - Objetivo: Encontrar a menor quantidade de moedas para dar um troco específico.
    - Abordagem: Seleciona as moedas de maior valor disponíveis primeiro (funciona bem com sistemas de moedas padrão).

### **Vantagens**

- **Simples de implementar**: A lógica gulosa é geralmente direta e compreensível.
- **Eficiente em tempo**: Em muitos casos, a complexidade é reduzida devido às decisões rápidas.

### **Desvantagens**

- **Não garantem solução ótima para todos os problemas**: Apenas para aqueles com as propriedades mencionadas (subestrutura ótima e escolha gulosa).
- **Irrevogabilidade**: Não há revisão de escolhas, o que pode levar a soluções subótimas.

### **Exemplo de Código (Problema do Troco em Python)**

Aqui está uma implementação básica de um algoritmo guloso:


```
def troco_guloso(valor, moedas):
    resultado = []
    for moeda in sorted(moedas, reverse=True):
        while valor >= moeda:
            valor -= moeda
            resultado.append(moeda)
    return resultado

# Uso
valor = 63
moedas = [1, 5, 10, 25, 50]
print("Moedas usadas:", troco_guloso(valor, moedas))
# Saída: Moedas usadas: [50, 10, 1, 1, 1]
```

### **Comparação com outras abordagens**

|Característica|Algoritmos Gulosos|Programação Dinâmica|
|---|---|---|
|**Escolhas**|Baseadas em decisões locais|Baseadas em tabelas globais|
|**Complexidade**|Geralmente mais rápida|Pode ser mais lenta, mas garante precisão|
|**Problemas adequados**|Problemas com subestrutura ótima|Problemas com subproblemas sobrepostos|
