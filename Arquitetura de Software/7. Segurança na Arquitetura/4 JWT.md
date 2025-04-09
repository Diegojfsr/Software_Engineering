**JWT** (abreviação de _JSON Web Token_) é um padrão aberto utilizado para transmitir informações de forma segura entre duas partes, geralmente um cliente e um servidor, como um **token de autenticação**. Essas informações são codificadas em formato **JSON (JavaScript Object Notation)** e, em muitos casos, assinadas digitalmente para garantir a integridade e a segurança.

### **Como funciona o JWT?**

O JWT é composto por três partes, separadas por pontos (`.`):
1. **Header (Cabeçalho):**
    - Contém informações sobre o tipo de token (geralmente "JWT") e o algoritmo de criptografia usado, como HS256 (HMAC com SHA-256).
2. **Payload (Corpo):**
    - Contém as **informações ou declarações (claims)** que estão sendo transmitidas. Exemplo de claims:
        - **Padrão:** `iss` (emissor), `exp` (tempo de expiração), `sub` (assunto).
        - **Personalizado:** Informações específicas da aplicação, como ID do usuário.
3. **Signature (Assinatura):**
    - É a parte responsável por garantir a integridade do token. Ela é gerada usando:
        - Header e Payload codificados em Base64.
        - Uma chave secreta compartilhada (ou chave privada em caso de assinatura assimétrica).
        - Algoritmo especificado no Header.

Exemplo de JWT: `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c`

### **Vantagens do JWT**

1. **Autossuficiência:** O token carrega as informações necessárias, sem a necessidade de consultas adicionais ao banco de dados.
2. **Desempenho:** Como é baseado em texto e leve, o JWT é rápido de processar e transportar.
3. **Segurança:** Pode ser assinado (para integridade) e criptografado (para confidencialidade, se necessário).
4. **Compatibilidade:** Funciona bem com diferentes linguagens de programação e APIs RESTful.

### **Uso do JWT**

1. **Autenticação:**
    - Após o login, o servidor gera um JWT e o retorna ao cliente.
    - O cliente armazena o token (geralmente no armazenamento local ou em cookies) e o utiliza para fazer requisições autenticadas ao servidor.
2. **Autorização:**
    - O servidor verifica o token para decidir quais recursos o usuário pode acessar.
3. **Troca de informações segura:**
    - O JWT pode ser usado para transmitir informações confiáveis entre duas partes (ex.: cliente e servidor).

### **Desafios e limitações**

- **Expiração e revogação:** Tokens expirados precisam ser gerenciados para evitar riscos. Além disso, revogar um token antes de expirar pode ser mais complicado sem um banco centralizado para controle.
- **Armazenamento seguro:** Um JWT mal armazenado pode ser interceptado (ex.: via ataques XSS ou CSRF).
- **Tamanho do token:** Como o token contém várias informações, ele pode crescer em tamanho e impactar redes com limitação de largura de banda.


