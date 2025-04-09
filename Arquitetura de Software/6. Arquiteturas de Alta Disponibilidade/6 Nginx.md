**Nginx** (pronunciado "Engine-X") é um software de código aberto amplamente utilizado como **servidor web**, **proxy reverso** e **balanceador de carga**. Ele foi criado por Igor Sysoev em 2004 com o foco em alto desempenho e baixo consumo de recursos, tornando-se uma escolha popular para aplicações que precisam lidar com milhões de conexões simultâneas.

### **Principais funções do Nginx**

1. **Servidor web:**
    - Utilizado para entregar conteúdo estático, como HTML, CSS, imagens e vídeos.
    - É conhecido por sua eficiência ao lidar com alta quantidade de acessos simultâneos.
2. **Proxy reverso:**
    - Atua como intermediário entre clientes (usuários) e servidores de aplicativos.
    - Reduz a carga nos servidores ao armazenar conteúdo em cache e permitir compressão de dados.
3. **Balanceador de carga:**
    - Distribui requisições entre vários servidores, garantindo desempenho e alta disponibilidade.
4. **Proxy para protocolos:**
    - Suporta HTTP, HTTPS, TCP e UDP, tornando-se versátil para diferentes tipos de serviços.

### **Características do Nginx**

- **Desempenho escalável:**
    - Utiliza um modelo baseado em eventos assíncronos, ideal para lidar com alta concorrência.
- **Configuração simples e flexível:**
    - Arquivos de configuração permitem ajustes finos para diversos casos de uso.
- **Múltiplos módulos:**
    - Expansível para incluir suporte a recursos como compressão gzip, cache avançado e controle de acesso.
- **Baixo consumo de memória:**
    - Comparado com outros servidores, é leve e eficiente.

### **Exemplos de uso prático**

1. **Servidor web estático:**
    - Hospedando páginas HTML e arquivos multimídia diretamente no Nginx.
2. **Proxy reverso com cache:**
    - Configuração para melhorar o desempenho de aplicativos, mantendo dados em cache para reduzir a carga do servidor backend.

    ```
    server {
        listen 80;
        server_name exemplo.com;
    
        location / {
            proxy_pass http://backend_server;
            proxy_cache cache_zone;
        }
    }
    ```

3. **Balanceamento de carga:**
    - Distribuir requisições entre vários servidores.

    ```
    upstream backend {
        server backend1.example.com;
        server backend2.example.com;
    }
    
    server {
        location / {
            proxy_pass http://backend;
        }
    }
    ```

### **Vantagens do Nginx**

- **Alta performance:** Ideal para aplicações que precisam lidar com grande volume de acessos.
- **Versatilidade:** Combina múltiplas funções (servidor web, proxy e balanceador de carga) em um só software.
- **Popularidade:** Ampla documentação e suporte da comunidade.

### **Desvantagens**

- **Curva de aprendizado:** Pode exigir algum esforço para configurar corretamente casos mais complexos.
- **Limitado para aplicativos dinâmicos:** Embora seja ótimo para conteúdo estático, pode depender de integração com outros servidores (ex.: Apache ou Node.js) para processamento dinâmico.

### **Casos de uso comuns**

- Hospedagem de sites com alto tráfego.
- Servir como proxy reverso para APIs REST.
- Balancear carga em sistemas distribuídos.
- Usar como ponto de entrada para clusters de microsserviços.


