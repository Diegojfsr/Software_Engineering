O **AWS ELB** (Amazon Elastic Load Balancer) é um serviço da Amazon Web Services que distribui automaticamente o tráfego de entrada de aplicações entre vários destinos, como instâncias EC2, contêineres e endereços IP, em uma ou mais zonas de disponibilidade. Ele é projetado para melhorar a **escalabilidade**, **disponibilidade** e **tolerância a falhas** de aplicativos na nuvem2.

### **Principais tipos de ELB**

1. **Application Load Balancer (ALB):**
    - Ideal para aplicativos baseados em HTTP e HTTPS.
    - Oferece roteamento avançado, como roteamento baseado em conteúdo ou host.
2. **Network Load Balancer (NLB):**
    - Projetado para lidar com tráfego de rede em alta escala e baixa latência.
    - Funciona com protocolos TCP e UDP.
3. **Gateway Load Balancer (GLB):**
    - Facilita a implantação de dispositivos de rede, como firewalls e sistemas de inspeção de tráfego.
4. **Classic Load Balancer (CLB):**
    - A geração anterior de balanceadores de carga, usada para aplicativos legados.

### **Benefícios do AWS ELB**

- **Escalabilidade automática:** Ajusta a capacidade do balanceador de carga conforme o tráfego aumenta ou diminui.
- **Alta disponibilidade:** Distribui o tráfego entre várias zonas de disponibilidade para garantir continuidade.
- **Monitoramento de integridade:** Verifica a saúde dos destinos registrados e envia tráfego apenas para os íntegros.
- **Segurança:** Suporte para terminação SSL/TLS e autenticação de certificados de clientes2.

### **Casos de uso**

- **Aplicativos modernos:** Escalar aplicativos baseados em contêineres ou sem servidor.
- **Redes híbridas:** Balancear carga entre recursos na AWS e on-premises.
- **Proteção contra falhas:** Garantir que o tráfego seja redirecionado para servidores ativos em caso de falhas2.

