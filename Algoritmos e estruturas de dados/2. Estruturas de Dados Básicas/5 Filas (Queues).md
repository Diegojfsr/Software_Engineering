**Filas (Queues)** são uma estrutura de dados linear que segue o princípio **FIFO** (_First In, First Out_), ou seja, o primeiro elemento inserido é o primeiro a ser removido. Uma fila pode ser imaginada como uma linha de pessoas esperando por atendimento: a pessoa que chegou primeiro é a primeira a ser atendida.

### **Características Principais**

1. **FIFO (First In, First Out)**: Os elementos são manipulados em ordem de chegada.
2. **Operações Básicas**:
    - **Enqueue**: Adiciona um elemento na fila (geralmente no final).
    - **Dequeue**: Remove o elemento da frente da fila.
    - **Peek (ou Front)**: Acessa o elemento da frente sem removê-lo.
    - **isEmpty**: Verifica se a fila está vazia.

### **Exemplo Visual**

```
Fila: [10, 20, 30]  
Enqueue(40): [10, 20, 30, 40]  # Adiciona 40 no final
Dequeue(): [20, 30, 40]        # Remove 10, que estava na frente
```

### **Tipos de Filas**

1. **Filas Simples**: Seguem o princípio FIFO básico.
2. **Filas Circulares**: O final da fila está conectado ao início, formando um ciclo. Utilizadas para otimizar o uso de memória.
3. **Filas Duplas (Deque)**: Permitem inserções e remoções de ambos os lados (frente e fim).
4. **Filas de Prioridade**: Cada elemento tem uma prioridade, e elementos com maior prioridade são removidos antes.

### **Vantagens**

1. **Gerenciamento de Tarefas**: Útil para cenários onde as tarefas devem ser executadas na ordem em que chegam.
2. **Simplicidade**: Fácil de implementar e entender.

### **Desvantagens**

1. **Acesso Limitado**: Apenas o elemento na frente pode ser acessado diretamente.
2. **Sem Busca Aleatória**: Para acessar elementos no meio da fila, é necessário percorrer toda a estrutura.

### **Exemplo em Código (Python)**

Aqui está uma implementação básica de uma fila:

```
class Fila:
    def __init__(self):
        self.itens = []

    def enqueue(self, item):
        self.itens.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.itens.pop(0)
        return "Fila vazia!"

    def peek(self):
        if not self.is_empty():
            return self.itens[0]
        return "Fila vazia!"

    def is_empty(self):
        return len(self.itens) == 0
```

**Uso:**

```
fila = Fila()
fila.enqueue(10)
fila.enqueue(20)
print(fila.peek())  # Saída: 10
fila.dequeue()
print(fila.peek())  # Saída: 20
```

### **Aplicações**

- **Gerenciamento de Processos em Sistemas Operacionais**: A fila de tarefas gerencia processos de forma FIFO.
- **Transferência de Dados em Redes**: Pacotes de dados são processados na ordem em que chegam.
- **Sistemas Bancários**: Filas simulam a ordem de atendimento de clientes.
- **Algoritmos de Busca (Ex.: BFS)**: Filas são usadas para explorar níveis em grafos.


