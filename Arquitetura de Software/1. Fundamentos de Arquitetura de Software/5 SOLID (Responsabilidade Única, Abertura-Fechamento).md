O SOLID é um conjunto de **princípios de design de software** criado para melhorar a qualidade, a manutenibilidade e a escalabilidade de sistemas. Esses princípios ajudam os desenvolvedores a projetarem software de maneira mais organizada e robusta. Vamos falar dos dois que você mencionou:

### **1. Princípio da Responsabilidade Única (Single Responsibility Principle - SRP)**

Cada classe, módulo ou componente deve ter **apenas uma razão para mudar**, ou seja, deve ser responsável por **apenas uma tarefa específica**.

- **Objetivo:** Evitar que uma única classe acumule várias responsabilidades, o que pode dificultar a manutenção e criar dependências desnecessárias.
- **Exemplo:** Em um sistema de pedidos, você pode ter uma classe para **gerenciar os dados do pedido** e outra para **processar o pagamento**. Cada uma tem uma responsabilidade clara e não interfere na outra.

### **2. Princípio Aberto/Fechado (Open/Closed Principle - OCP)**

Os componentes do sistema devem ser projetados para serem:

- **Abertos para extensões:** É possível adicionar novas funcionalidades sem modificar o código existente.
- **Fechados para modificações:** Alterações no sistema não devem impactar diretamente os componentes já implementados.
- **Objetivo:** Garantir que o sistema seja expansível sem introduzir novos bugs ou riscos às funcionalidades existentes.
- **Exemplo:** Em um sistema de cálculo de impostos, você pode criar uma interface genérica de cálculo e implementar novas classes para impostos específicos. Se um novo imposto precisar ser calculado, basta adicionar uma nova classe, sem alterar as já existentes.

Além desses, os outros princípios do SOLID são:

- **Liskov Substitution Principle (Substituição de Liskov)**
- **Interface Segregation Principle (Segregação de Interfaces)**
- **Dependency Inversion Principle (Inversão de Dependências)**

## Detalhes e exemplos práticos
Vamos nos aprofundar em cada um dos princípios do SOLID, com detalhes e exemplos práticos para tornar tudo mais claro.

### **1. Princípio da Responsabilidade Única (SRP - Single Responsibility Principle)**

O SRP estabelece que uma classe ou módulo deve ter **apenas uma responsabilidade**, ou seja, uma razão para mudar.

- **Por quê?** Quando uma classe faz muitas coisas ao mesmo tempo, mudanças em uma responsabilidade podem afetar outras, criando um "efeito cascata" e dificultando a manutenção.
- **Como implementar?** Divida responsabilidades grandes em componentes menores e especializados.

**Exemplo prático:** Imagine um sistema para gerenciar livros em uma livraria:

- Classe que faz **gerenciamento de estoque**.
- Classe que cuida da **logística de envio**.
- Classe que processa **pagamentos**.

Se tudo fosse tratado por uma única classe, qualquer alteração em uma funcionalidade afetaria todas as outras.

Código para ilustrar:

```
class Estoque:
    def atualizar_estoque(self, livro, quantidade):
        # Código para atualizar estoque
        pass

class Pagamento:
    def processar_pagamento(self, pedido):
        # Código para processar pagamento
        pass
```

Dessa forma, cada classe tem sua responsabilidade única.

### **2. Princípio Aberto/Fechado (OCP - Open/Closed Principle)**

Esse princípio sugere que o sistema deve ser:

- **Aberto para extensões:** Podemos adicionar novas funcionalidades facilmente.
- **Fechado para modificações:** O código existente não deve ser alterado ao introduzir algo novo.

**Por quê?** Isso reduz o risco de bugs ao modificar algo que já está funcionando e torna o código mais estável.

**Exemplo prático:** Imagine um sistema que calcula diferentes tipos de descontos para uma loja. Podemos projetá-lo para que novos descontos sejam adicionados sem alterar a lógica existente:

```
from abc import ABC, abstractmethod

class Desconto(ABC):
    @abstractmethod
    def calcular(self, valor):
        pass

class DescontoFidelidade(Desconto):
    def calcular(self, valor):
        return valor * 0.9  # 10% de desconto

class DescontoPromocao(Desconto):
    def calcular(self, valor):
        return valor * 0.8  # 20% de desconto
```

Se precisar de um novo tipo de desconto, basta criar outra classe que implemente a interface `Desconto`, sem modificar as classes existentes.

### **3. Princípio da Substituição de Liskov (LSP - Liskov Substitution Principle)**

Subclasses devem poder substituir suas classes base sem alterar o funcionamento do sistema.

- **Por quê?** Garante consistência no comportamento ao utilizar subclasses.
- **Como implementar?** Certifique-se de que as subclasses respeitem a interface e o comportamento esperado da classe base.

**Exemplo prático:** Imagine um sistema com a classe base `Forma` e subclasses `Retangulo` e `Quadrado`:

```
class Forma:
    def calcular_area(self):
        pass

class Retangulo(Forma):
    def __init__(self, largura, altura):
        self.largura = largura
        self.altura = altura

    def calcular_area(self):
        return self.largura * self.altura
```

Se `Quadrado` herdar de `Retangulo`, precisamos garantir que o comportamento de `calcular_area` seja consistente e não cause erros.

### **4. Princípio da Segregação de Interfaces (ISP - Interface Segregation Principle)**

Uma classe não deve ser obrigada a implementar métodos que não utiliza. Ou seja, interfaces devem ser específicas para o uso necessário.

- **Por quê?** Torna o sistema mais limpo e evita a implementação de métodos desnecessários.
- **Exemplo prático:** Considere um sistema com interfaces separadas para diferentes tipos de dispositivos:

```
class Impressora:
    def imprimir(self):
        pass

class Scanner:
    def escanear(self):
        pass
```

Dessa forma, uma impressora que não escaneia não precisa implementar métodos de escaneamento.

### **5. Princípio da Inversão de Dependência (DIP - Dependency Inversion Principle)**

Módulos de alto nível não devem depender de módulos de baixo nível; ambos devem depender de abstrações.

- **Por quê?** Garante flexibilidade e reduz o impacto de mudanças em dependências específicas.
- **Como implementar?** Utilize interfaces ou injeção de dependência para desacoplar o código.

**Exemplo prático:** Um sistema que envia notificações pode ser implementado com injeção de dependência:

```
class Notificacao(ABC):
    @abstractmethod
    def enviar(self, mensagem):
        pass

class Email(Notificacao):
    def enviar(self, mensagem):
        print(f"Enviando email: {mensagem}")

class Sistema:
    def __init__(self, notificacao: Notificacao):
        self.notificacao = notificacao

    def processar(self, mensagem):
        self.notificacao.enviar(mensagem)

# Uso
email = Email()
sistema = Sistema(email)
sistema.processar("Olá, este é um teste.")
```

Esses princípios são como "norteadores" para projetar sistemas mais limpos, adaptáveis e fáceis de evoluir.

