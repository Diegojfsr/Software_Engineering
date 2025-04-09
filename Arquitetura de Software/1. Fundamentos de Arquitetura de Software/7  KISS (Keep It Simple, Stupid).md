O princípio **KISS** (_Keep It Simple, Stupid_, ou "Mantenha Simples, Idiota") é uma abordagem de design que defende a simplicidade como a chave para criar sistemas eficazes e funcionais. A ideia central é evitar complexidade desnecessária, tornando o sistema mais fácil de entender, implementar e manter.

### **Por que o KISS é importante?**

- **Facilidade de manutenção:** Sistemas simples são menos propensos a erros e mais fáceis de corrigir ou atualizar.
- **Menor risco:** Soluções complexas podem introduzir mais falhas e dependências inesperadas.
- **Agilidade:** Soluções simples permitem desenvolvimento mais rápido e eficiente.

### **Como aplicar o KISS?**

1. **Evitar complexidade desnecessária:** Projete soluções que atendam às necessidades diretamente, sem exagerar na sofisticação ou nos detalhes.
2. **Manter o foco na funcionalidade essencial:** Concentre-se no objetivo principal do sistema, evitando adicionar recursos ou lógica que não são realmente necessários.
3. **Dividir para conquistar:** Se o sistema for grande, divida-o em partes menores e independentes, cada uma com um propósito claro.

### **Exemplo prático:**

Imagine que você está desenvolvendo um aplicativo para calcular a soma de dois números.
**Errado:** Criar uma lógica complexa com múltiplas classes, validadores e interfaces desnecessárias.
**Certo:** Manter o código direto e funcional:

```
def somar(a, b):
    return a + b

print(somar(5, 3))  # Resultado: 8
```

O princípio KISS lembra que **"menos é mais"** em muitos casos, especialmente no desenvolvimento de software.

