O **Apache Cassandra** é um sistema de gerenciamento de banco de dados NoSQL projetado para lidar com grandes volumes de dados distribuídos entre vários servidores, oferecendo alta escalabilidade, desempenho e tolerância a falhas. Ele é particularmente conhecido por ser extremamente eficaz em casos de uso que exigem alta disponibilidade sem ponto único de falha. Foi inicialmente desenvolvido pelo Facebook e é mantido pela **Apache Software Foundation**.

### **Características principais do Cassandra**

1. **Modelo de dados baseado em colunas:**
    - Os dados são organizados em **families (famílias de colunas)**, o que permite consultas rápidas para grandes volumes de dados.
2. **Descentralizado:**
    - Todos os nós no cluster têm o mesmo papel, eliminando pontos únicos de falha.
3. **Alta escalabilidade horizontal:**
    - É fácil adicionar mais servidores ao cluster para suportar maior demanda.
4. **Tolerância a falhas:**
    - Suporta replicação automática dos dados entre nós, garantindo disponibilidade mesmo em caso de falhas.
5. **Consistência configurável:**
    - Permite ajustar o nível de consistência das operações (ex.: forte ou eventual), dependendo do caso de uso.
6. **Baseado no modelo CAP:**
    - Prioriza **Disponibilidade** e **Partição** em detrimento de **Consistência forte**, embora permita flexibilidade nos níveis de consistência.

### **Vantagens do Cassandra**

- **Alta disponibilidade:** Projetado para sistemas que não podem ter interrupções, como e-commerce ou IoT.
- **Performance impressionante:** É altamente eficiente para leituras e gravações rápidas em grande escala.
- **Escalabilidade:** Cresce horizontalmente adicionando novos nós.
- **Distribuído por design:** Ideal para infraestruturas globais.

### **Desvantagens do Cassandra**

- **Curva de aprendizado:** Sua configuração e otimização podem ser mais complexas do que outros bancos de dados NoSQL.
- **Menos eficiente para transações complexas:** Como bancos baseados em colunas, ele não é ideal para sistemas que exigem transações ACID fortes.

### **Casos de uso do Cassandra**

- **Sistemas de recomendação:** Para armazenar grandes volumes de dados comportamentais de usuários.
- **IoT:** Processamento em tempo real de dados de dispositivos conectados.
- **E-commerce:** Registro de atividades dos clientes e logs de transações.
- **Redes sociais:** Para armazenar informações de feeds de atividades e conexões entre usuários.

### **Exemplo prático**

Criar uma tabela simples em Cassandra para registrar informações de usuários:

```
CREATE KEYSPACE usuarios_comercio
WITH replication = {'class': 'SimpleStrategy', 'replication_factor': '3'};

USE usuarios_comercio;

CREATE TABLE usuarios (
    id UUID PRIMARY KEY,
    nome TEXT,
    email TEXT,
    registro TIMESTAMP
);

INSERT INTO usuarios (id, nome, email, registro) VALUES (uuid(), 'Diego', 'diego@email.com', toTimestamp(now()));
```

O Cassandra é amplamente utilizado em arquiteturas modernas, como microsserviços e sistemas baseados em eventos, onde alta disponibilidade e escala global são essenciais.


