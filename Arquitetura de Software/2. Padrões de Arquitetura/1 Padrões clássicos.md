Os **padrões clássicos de projeto de software** são soluções reutilizáveis e consagradas para problemas comuns no desenvolvimento. Eles ajudam a criar sistemas bem estruturados, fáceis de manter e escaláveis. Abaixo estão alguns dos padrões mais conhecidos, organizados em categorias:

### **1. Padrões de Criação**

Esses padrões lidam com a forma como objetos e classes são criados, promovendo flexibilidade e reutilização.

- **Singleton:** Garante que uma classe tenha apenas uma instância e fornece um ponto de acesso global a ela.
- **Factory Method:** Define uma interface para criar objetos, permitindo que as subclasses decidam qual classe instanciar.
- **Abstract Factory:** Fornece uma interface para criar famílias de objetos relacionados ou dependentes sem especificar suas classes concretas.
- **Builder:** Separa a construção de um objeto da sua representação, permitindo criar diferentes representações com o mesmo processo.
- **Prototype:** Cria novos objetos copiando uma instância existente.

### **2. Padrões Estruturais**

Esses padrões tratam da composição de classes e objetos para formar estruturas maiores.

- **Adapter:** Converte a interface de uma classe em outra interface que o cliente espera, permitindo compatibilidade entre sistemas diferentes.
- **Composite:** Permite tratar objetos individuais e grupos de objetos de forma uniforme.
- **Decorator:** Adiciona funcionalidades a um objeto dinamicamente, sem alterar sua estrutura original.
- **Facade:** Fornece uma interface simplificada para um conjunto de interfaces mais complexas.
- **Bridge:** Desacopla uma abstração da sua implementação, permitindo que as duas evoluam separadamente.
- **Proxy:** Fornece um substituto ou representante para controlar o acesso a outro objeto.

### **3. Padrões Comportamentais**

Esses padrões se concentram em como objetos interagem e se comunicam.

- **Observer:** Define uma dependência entre objetos, de forma que quando um muda de estado, os dependentes sejam notificados.
- **Strategy:** Permite definir uma família de algoritmos, encapsulá-los e selecionar o algoritmo apropriado no momento da execução.
- **Command:** Encapsula uma solicitação como um objeto, permitindo parametrização e controle de execução.
- **Chain of Responsibility:** Passa uma solicitação por uma cadeia de handlers, onde cada um decide se processa ou a encaminha.
- **State:** Permite que um objeto altere seu comportamento quando seu estado interno muda.
- **Template Method:** Define o esqueleto de um algoritmo, delegando etapas específicas para subclasses.
- **Visitor:** Permite adicionar novos comportamentos a objetos sem alterar suas estruturas.

Esses padrões foram descritos pela primeira vez no livro clássico _Design Patterns: Elements of Reusable Object-Oriented Software_ (1994), escrito por Erich Gamma, Richard Helm, Ralph Johnson e John Vlissides, conhecidos como "Gang of Four" (GoF).

