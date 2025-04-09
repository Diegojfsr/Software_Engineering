**Pilhas (Stacks)** são um tipo de estrutura de dados linear que segue o princípio **LIFO** (_Last In, First Out_), ou seja, o último elemento inserido é o primeiro a ser removido. Imagine uma pilha de pratos: o último prato colocado no topo é o primeiro a ser retirado.

### **Características Principais**

1. **LIFO (Last In, First Out)**: Elementos são acessados de acordo com a ordem em que foram adicionados, sendo o último o primeiro a sair.
2. **Operações Básicas**:
    - **Push**: Adiciona um elemento no topo da pilha.
    - **Pop**: Remove o elemento do topo da pilha.
    - **Peek (ou Top)**: Acessa o elemento no topo sem removê-lo.
    - **isEmpty**: Verifica se a pilha está vazia.

### **Exemplo Visual**

```
Pilha: [10, 20, 30]  
Push(40): [10, 20, 30, 40]  # Adiciona 40 no topo
Pop(): [10, 20, 30]         # Remove 40 do topo
```

### **Vantagens**

1. **Simples de Implementar**: É fácil criar e manipular pilhas.
2. **Útil em Cenários Específicos**: Como ao resolver problemas de recursão, analisadores sintáticos ou _undo/redo_ em editores de texto.

### **Desvantagens**

1. **Acesso Limitado**: Só o elemento no topo é acessível diretamente.
2. **Sem Busca Aleatória**: Não é possível acessar elementos do meio da pilha sem removê-los.

### **Exemplo em Código (Python)**

Aqui está uma implementação básica de uma pilha:

```
class Pilha:
    def __init__(self):
        self.itens = []

    def push(self, item):
        self.itens.append(item)

    def pop(self):
        if not self.is_empty():
            return self.itens.pop()
        return "Pilha vazia!"

    def peek(self):
        if not self.is_empty():
            return self.itens[-1]
        return "Pilha vazia!"

    def is_empty(self):
        return len(self.itens) == 0
```

**Uso:**

```
pilha = Pilha()
pilha.push(10)
pilha.push(20)
print(pilha.peek())  # Saída: 20
pilha.pop()
print(pilha.peek())  # Saída: 10
```

### **Aplicações**

- **Algoritmos Recursivos**: Pilhas são usadas para gerenciar chamadas de funções recursivas.
- **Navegação no Navegador**: Gerenciar o histórico de páginas visitadas (botões de _voltar_ e _avançar_).
- **Algoritmos de Backtracking**: Como resolver labirintos ou problemas como Sudoku.
- **Avaliação de Expressões**: Pilhas são usadas para avaliar expressões matemáticas ou converter entre notações (ex.: infixa para pós-fixa).

