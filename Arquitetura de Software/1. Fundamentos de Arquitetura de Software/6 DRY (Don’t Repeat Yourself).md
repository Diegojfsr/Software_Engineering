O princípio **DRY** (_Don’t Repeat Yourself_, ou "Não se Repita") é um dos pilares do desenvolvimento de software bem projetado. Ele incentiva os desenvolvedores a evitarem duplicação de código ou lógica, garantindo que cada unidade de informação ou funcionalidade esteja representada de forma única e centralizada dentro de um sistema.

### **Por que o DRY é importante?**

- **Redução de redundância:** Diminuir a duplicação torna o código mais limpo e organizado.
- **Facilidade de manutenção:** Quando um ponto central é modificado, todas as partes do sistema que dependem dele são automaticamente atualizadas. Isso evita que alterações sejam feitas em vários lugares.
- **Prevenção de erros:** Ter lógica duplicada pode levar a inconsistências ou bugs difíceis de identificar.

### **Como aplicar o DRY?**

1. **Centralizar código comum:** Em vez de duplicar o código em várias partes, coloque-o em funções reutilizáveis, classes ou módulos.

    **Exemplo prático:** Errado (duplicando lógica):

    ```
    total = preco_unitario * quantidade
    print(f"Total: {total}")
    total_com_taxa = preco_unitario * quantidade * 1.1
    print(f"Total com taxa: {total_com_taxa}")
    ```

    Certo (centralizando lógica em uma função):

    ```
    def calcular_total(preco_unitario, quantidade, taxa=1):
        return preco_unitario * quantidade * taxa
    
    total = calcular_total(100, 2)
    print(f"Total: {total}")
    total_com_taxa = calcular_total(100, 2, 1.1)
    print(f"Total com taxa: {total_com_taxa}")
    ```

2. **Utilizar abstrações:** Crie classes ou interfaces que encapsulem comportamento comum.

3. **Evitar copiar/colar:** Sempre que houver a necessidade de repetir código ou lógica, considere refatorar o sistema.

### **Aplicações do DRY no cotidiano do desenvolvimento**

- **Base de dados:** Garanta que os dados sejam armazenados de forma única, sem repetição desnecessária.
- **Estilo CSS:** Evite duplicar estilos; utilize classes reutilizáveis no código.
- **Lógica de negócios:** Centralize cálculos ou validações em funções comuns para reutilizá-las.

Esse princípio é essencial para manter os sistemas mais simples, robustos e fáceis de evoluir.



