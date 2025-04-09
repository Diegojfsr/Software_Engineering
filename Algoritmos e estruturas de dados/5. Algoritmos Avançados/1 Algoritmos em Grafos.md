**Algoritmos em grafos** são métodos e técnicas usadas para resolver problemas relacionados a grafos, que consistem em **vértices** (nós) e **arestas** (conexões). Esses algoritmos exploram as relações entre os vértices e as arestas para realizar tarefas como busca, caminhos mais curtos, conectividade, ciclos, e muito mais.

### **Tipos de Algoritmos em Grafos**

Aqui estão alguns dos principais algoritmos usados em grafos:

#### **1. Algoritmos de Busca**

Esses algoritmos exploram os vértices de um grafo de forma sistemática.

- **Busca em Largura (BFS - Breadth-First Search)**:
    - Explora um grafo em **camadas**, visitando todos os vizinhos de um vértice antes de avançar para os próximos níveis.
    - Usado para verificar conectividade, encontrar o caminho mais curto em grafos **não ponderados**, etc.
    - Complexidade: O(V+E)O(V + E), onde VV é o número de vértices e EE é o número de arestas.
- **Busca em Profundidade (DFS - Depth-First Search)**:
    - Explora o grafo indo o mais fundo possível em uma ramificação antes de retroceder.
    - Usado para detectar ciclos, classificar topologicamente e encontrar componentes fortemente conectados
    - Complexidade: O(V+E)O(V + E).

#### **2. Algoritmos de Caminhos Mínimos**

Estes algoritmos encontram o caminho mais curto entre dois ou mais vértices.

- **Dijkstra**:
    - Funciona em grafos **ponderados com pesos não negativos**.
    - Usa uma fila de prioridade para escolher o vértice com a menor distância acumulada.
    - Complexidade: O((V+E)log⁡V)O((V + E) \log V).
- **Bellman-Ford**:
    - Resolve o problema de caminhos mínimos em grafos que **podem conter arestas com pesos negativos**.
    - Complexidade: O(VE)O(VE).
- **Floyd-Warshall**:
    - Encontra o caminho mais curto entre todos os pares de vértices (**all-pairs shortest path**).
    - Complexidade: O(V3)O(V^3).

#### **3. Algoritmos de Conectividade**

Estes verificam ou calculam conectividade em um grafo.

- **Componentes Fortemente Conectados (SCCs)**:
    - Encontram subconjuntos de vértices em grafos direcionados onde todos os vértices são mutuamente alcançáveis.
    - Algoritmo de Kosaraju ou Tarjan.
- **Árvore Geradora Mínima (MST - Minimum Spanning Tree)**:
    - Conecta todos os vértices de um grafo **não direcionado e ponderado** com o menor custo total.
    - **Algoritmo de Kruskal**: Escolhe arestas em ordem crescente de peso.
    - **Algoritmo de Prim**: Constrói a árvore adicionando vértices vizinhos ao conjunto já conectado.

#### **4. Algoritmos de Ciclos**

- **Detecção de Ciclos**:
    - Usa DFS ou outras abordagens para identificar se existem ciclos em grafos.
    - Importante em grafos direcionados para verificar dependências circulares.
- **Ciclo Hamiltoniano**:
    - Encontra um ciclo que visita todos os vértices exatamente uma vez.
    - Problema NP-completo.
- **Ciclo Euleriano**:
    - Encontra um caminho que percorre todas as arestas exatamente uma vez.
    - Grafos devem atender à propriedade de Euler (todos os vértices têm grau par, exceto no início e fim de um caminho).

### **Aplicações de Algoritmos em Grafos**

- **Redes de Transporte**: Para encontrar rotas otimizadas, como no Google Maps.
- **Redes Sociais**: Para sugerir amigos ou detectar comunidades.
- **Planejamento de Projetos**: Usando grafos direcionados acíclicos (DAGs) para gerenciar dependências.
- **Rastreamento de Pacotes**: Em redes de computadores.
- **Ciência de Dados**: Para análise de grafos em big data.

