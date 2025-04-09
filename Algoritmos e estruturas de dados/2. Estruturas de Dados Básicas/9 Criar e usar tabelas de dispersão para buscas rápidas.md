Para criar e usar **tabelas de dispersão (hash tables)** para buscas rápidas, é necessário entender como funciona a associação de **chaves** a **valores** e como a **função hash** otimiza o acesso aos dados. Aqui estão os passos principais:

### **1. Planejar a Estrutura da Tabela**

Decida como os dados serão representados:
- **Chave:** Identificador único (por exemplo, um nome ou código).
- **Valor:** Informação associada à chave (por exemplo, um endereço ou número).

Exemplo:

```
Chave: "Diego" -> Valor: "Engenheiro de Software"
```

### **2. Escolher ou Criar uma Função Hash**

A **função hash** converte a chave em um índice válido no array que compõe a tabela. O ideal é que a função seja:
- **Rápida:** Produza o índice rapidamente.
- **Eficiente:** Distribua as chaves uniformemente para evitar colisões.

Exemplo básico de função hash:

```
def funcao_hash(chave, tamanho_da_tabela):
    return sum(ord(caractere) for caractere in chave) % tamanho_da_tabela
```

Essa função calcula o índice somando os valores ASCII de cada caractere da chave e usando o operador módulo para se ajustar ao tamanho da tabela.

### **3. Criar e Popular a Tabela de Dispersão**

Implemente a tabela como um array ou lista, com suporte para operações de **inserção**, **busca** e **remoção**.
Exemplo em Python:

```
class HashTable:
    def __init__(self, tamanho):
        self.tabela = [None] * tamanho

    def funcao_hash(self, chave):
        return sum(ord(caractere) for caractere in chave) % len(self.tabela)

    def inserir(self, chave, valor):
        indice = self.funcao_hash(chave)
        if not self.tabela[indice]:
            self.tabela[indice] = []
        self.tabela[indice].append((chave, valor))

    def buscar(self, chave):
        indice = self.funcao_hash(chave)
        if self.tabela[indice]:
            for k, v in self.tabela[indice]:
                if k == chave:
                    return v
        return None

    def remover(self, chave):
        indice = self.funcao_hash(chave)
        if self.tabela[indice]:
            for i, (k, v) in enumerate(self.tabela[indice]):
                if k == chave:
                    del self.tabela[indice][i]
                    return True
        return False
```

**Uso:**

```
# Criando uma tabela de dispersão com tamanho 10
hash_table = HashTable(10)
hash_table.inserir("Diego", "Engenheiro de Software")
hash_table.inserir("Alice", "Designer")

# Buscando dados
print(hash_table.buscar("Diego"))  # Saída: Engenheiro de Software

# Removendo dados
hash_table.remover("Alice")
print(hash_table.buscar("Alice"))  # Saída: None
```

### **4. Resolver Colisões**

As colisões ocorrem quando duas chaves diferentes geram o mesmo índice. As abordagens para lidar com isso incluem:

1. **Encadeamento Separado:** Armazenar múltiplos valores no mesmo índice usando listas ligadas.
2. **Probing Linear ou Quadrático:** Procurar o próximo índice disponível no array.

### **5. Realizar Buscas Rápidas**

Para buscar um valor:
- Calcule o índice da chave usando a função hash.
- Acesse o índice no array.
- Se houver várias chaves armazenadas no mesmo índice, compare diretamente as chaves.

### **Vantagens das Tabelas de Dispersão**

- Permitem buscas rápidas em tempo **O(1)** no melhor caso.
- São extremamente úteis para cenários como cache de dados, indexação e verificação de duplicatas.


