O **Prometheus** é uma ferramenta de monitoramento de código aberto desenvolvida para coletar métricas de sistemas e aplicativos, armazená-las em um banco de dados **time-series** (baseado em séries temporais) e permitir que você analise e crie alertas com base nessas métricas. Ele é amplamente utilizado em arquiteturas modernas, especialmente em ambientes de contêineres e microsserviços.

### **Principais características do Prometheus**

1. **Modelo baseado em pull:** O Prometheus coleta métricas periodicamente ao consultar endpoints configurados (_scraping_).
2. **Banco de dados de séries temporais:** Armazena dados com carimbo de tempo para análise de tendências.
3. **Consultas com PromQL:** Possui sua própria linguagem de consulta para extrair e analisar dados coletados.
4. **Alertmanager:** Envia alertas com base em regras definidas.
5. **Integração com Grafana:** Permite criar dashboards avançados para visualização de métricas.

### **Como usar o Prometheus?**

1. **Instalação:**
    - Baixe e instale o Prometheus no site oficial.
    - Escolha entre executar em servidores locais, contêineres Docker ou clusters Kubernetes.
2. **Configuração:**
    - Configure o arquivo `prometheus.yml` para definir quais endpoints o Prometheus deve monitorar.
    - Exemplo de configuração:

        ```
        scrape_configs:
          - job_name: 'minha_aplicacao'
            static_configs:
              - targets: ['localhost:9090']
        ```

3. **Expor métricas:**
    - Aplicativos precisam expor métricas em um formato que o Prometheus entenda.
    - Ferramentas como o **client libraries** (ex.: `prometheus-client` para Python ou `Prometheus.Net` para .NET) facilitam a integração.
    - Exemplo em Python:

        ```
        from prometheus_client import start_http_server, Counter
        
        c = Counter('requests_total', 'Total de requisições')
        
        def process_request():
            c.inc()
        
        start_http_server(8000)
        ```

4. **Consultas com PromQL:**
    - Use o Prometheus para executar consultas com a linguagem PromQL.
    - Exemplo de consulta: `rate(http_requests_total[5m])` (taxa de requisições HTTP nos últimos 5 minutos).
5. **Visualização com Grafana:**
    - Conecte o Prometheus ao Grafana para criar dashboards e gráficos interativos.
    - Configurar o Grafana é simples, basta adicionar o Prometheus como fonte de dados.
6. **Alertas:**
    - Configure o **Alertmanager** para enviar notificações por e-mail, Slack ou outras plataformas quando métricas atingirem limites pré-definidos.
    - Exemplo: Alertar quando o uso de CPU ultrapassar 90%.

### **Benefícios do Prometheus**

- **Alta escalabilidade:** Suporta o monitoramento de grandes sistemas distribuídos.
- **Amplo suporte:** Compatível com várias linguagens e tecnologias, como Python, Java, Kubernetes e Docker.
- **Comunidade ativa:** Amplo suporte de documentação e plugins.


