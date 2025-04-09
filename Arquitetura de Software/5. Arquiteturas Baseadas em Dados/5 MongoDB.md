**MongoDB** é um banco de dados **NoSQL** baseado em documentos, conhecido por sua flexibilidade e capacidade de lidar com grandes volumes de dados não estruturados ou semiestruturados. Ele armazena os dados em um formato JSON/BSON, permitindo que sejam facilmente compreendidos e manipulados. Foi projetado para ser altamente escalável e rápido, sendo uma escolha popular para aplicativos modernos que exigem desempenho e adaptabilidade.

### **Características principais do MongoDB**

1. **Modelo baseado em documentos:**
    - Os dados são armazenados como documentos no formato JSON ou BSON.
    - Cada documento é independente e pode ter diferentes conjuntos de campos.
2. **Sem esquema rígido:**
    - Não há necessidade de definir um esquema fixo, o que oferece flexibilidade para modificar a estrutura dos dados conforme necessário.
3. **Escalabilidade horizontal:**
    - Utiliza o conceito de **sharding** para dividir os dados entre vários servidores, permitindo lidar com grandes volumes de dados.
4. **Consultas poderosas:**
    - Suporta consultas complexas, agregações e filtragem de dados.
5. **Alta performance:**
    - É otimizado para leituras e escritas rápidas, ideal para sistemas com alta demanda.

### **Vantagens do MongoDB**

- **Flexibilidade:** Permite armazenar documentos sem a necessidade de seguir um esquema rígido.
- **Escalabilidade:** Projetado para crescer horizontalmente, adicionando mais servidores conforme a demanda.
- **Dados ricos:** O formato de documentos JSON/BSON permite incluir informações estruturadas e complexas.
- **Fácil integração:** Possui drivers para várias linguagens de programação, como Python, Node.js, Java, e mais.

### **Desvantagens do MongoDB**

- **Menor suporte a transações complexas:** Embora suporte transações, bancos relacionais ainda são mais robustos para casos de uso intensivo.
- **Consistência eventual:** Em sistemas distribuídos, pode ocorrer atrasos na sincronização de dados.

### **Aplicações do MongoDB**

1. **Aplicações web:** Ideal para sistemas que armazenam dados dinâmicos e variáveis, como e-commerce e redes sociais.
2. **Big Data:** Processamento e análise de grandes volumes de dados semiestruturados.
3. **Internet das Coisas (IoT):** Para gerenciar e armazenar dados de sensores e dispositivos.
4. **APIs modernas:** Perfeito para APIs que retornam respostas em JSON.

### **Exemplo prático**

Criando um banco e inserindo um documento com MongoDB:

```
// Conectar ao banco
use loja;

// Inserir um documento na coleção "produtos"
db.produtos.insertOne({
    nome: "Notebook",
    preco: 2500.00,
    estoque: 15,
    categoria: "Eletrônicos"
});

// Buscar todos os documentos
db.produtos.find();
```

