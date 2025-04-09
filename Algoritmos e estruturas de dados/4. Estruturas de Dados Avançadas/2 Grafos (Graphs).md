**Grafos (Graphs)** são estruturas de dados usadas para representar relacionamentos entre objetos. Eles consistem em **vértices** (ou nós) e **arestas** que conectam esses vértices. Grafos podem modelar diversos problemas do mundo real, como redes sociais, mapas, sistemas de transporte, e muito mais.

### **Estrutura de um Grafo**

1. **Vértices (Nodes)**:
    - São os pontos de conexão no grafo. Cada vértice pode representar um objeto ou entidade.
    - Exemplo: Em um mapa, os vértices podem ser cidades.
2. **Arestas (Edges)**:
    - São as conexões entre os vértices. As arestas podem ter:
        - **Direção**: Em um grafo direcionado, a conexão vai de um vértice a outro em um sentido específico.
        - **Peso**: Representa o custo, distância ou outra medida associada à conexão.
    - Exemplo: Em um mapa, as arestas podem representar estradas e suas distâncias.

### **Tipos de Grafos**

1. **Grafo Direcionado**:
    - As conexões possuem direção.
    - Exemplo: Fluxos de tráfego onde as ruas têm sentido único.
2. **Grafo Não Direcionado**:
    - As conexões não possuem direção, ou seja, é possível percorrer nos dois sentidos.
    - Exemplo: Relacionamentos de amizade em redes sociais.
3. **Grafo Ponderado**:
    - As arestas possuem um peso associado.
    - Exemplo: Mapas com distâncias entre cidades.
4. **Grafo Não Ponderado**:
    - Não há peso nas arestas. Elas simplesmente indicam uma conexão.
    - Exemplo: Estrutura de um jogo de tabuleiro.

### **Representação de Grafos**

Existem várias formas de representar grafos em programação:

1. **Lista de Adjacência**:
    - Usa listas para armazenar quais vértices estão conectados.
    - Exemplo:

        ```
        Vértices: [A, B, C]
        Arestas: 
        A -> [B, C]
        B -> [A, C]
        C -> [A, B]
        ```

2. **Matriz de Adjacência**:
    - Usa uma matriz para indicar conexões entre vértices.
    - Exemplo:

        ```
          A  B  C
        A 0  1  1
        B 1  0  1
        C 1  1  0
        ```

### **Principais Algoritmos para Grafos**

1. **Busca em Largura (Breadth-First Search, BFS)**:
    - Explora todos os vértices de um nível antes de avançar para o próximo.
    - Usado para encontrar o caminho mais curto em grafos não ponderados.
2. **Busca em Profundidade (Depth-First Search, DFS)**:
    - Explora o máximo possível em um único ramo antes de retroceder.
    - Usado para verificar conexões ou detectar ciclos.
3. **Algoritmo de Dijkstra**:
    - Encontra o caminho mais curto em grafos ponderados.
    - Exemplo: Calcular rotas de GPS.
4. **Algoritmo de Kruskal e Prim**:
    
    - Encontram a Árvore Geradora Mínima (_Minimum Spanning Tree_), que conecta todos os vértices com o menor custo.

### **Aplicações de Grafos**

- **Redes Sociais**: Modelar conexões entre usuários.
- **Sistemas de Transporte**: Representar caminhos e calcular rotas.
- **Web**: Representar links entre páginas.
- **Computação Gráfica**: Representar relações entre elementos gráficos.
- **Ciência e Engenharia**: Simulação de circuitos ou fluxos em sistemas.


