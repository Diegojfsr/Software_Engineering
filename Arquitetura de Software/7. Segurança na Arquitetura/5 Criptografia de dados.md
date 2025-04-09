**Criptografia de dados** é o processo de proteger informações convertendo-as de um formato legível para um formato codificado, chamado de **texto cifrado** (ciphertext). Essa técnica torna os dados ilegíveis sem uma chave ou processo de decodificação apropriado, garantindo que apenas pessoas ou sistemas autorizados possam acessar e entender as informações.

### **Como funciona a criptografia?**

A criptografia usa algoritmos matemáticos para embaralhar os dados. Existem dois componentes principais no processo:

1. **Texto plano:** Os dados originais legíveis.
2. **Texto cifrado:** O resultado após os dados serem codificados.

Para decifrar os dados, é necessário uma **chave criptográfica**, que pode ser simétrica ou assimétrica.

### **Tipos de criptografia**

1. **Criptografia Simétrica:**
    - Usa uma única chave para criptografar e decifrar os dados.
    - **Exemplo:** O algoritmo AES (Advanced Encryption Standard).
    - **Vantagem:** Rápido e eficiente para grandes volumes de dados.
    - **Desvantagem:** Requer que a chave seja compartilhada com segurança entre as partes.
2. **Criptografia Assimétrica:**
    - Usa duas chaves: uma **chave pública** para criptografar e uma **chave privada** para decifrar.
    - **Exemplo:** O algoritmo RSA.
    - **Vantagem:** Mais segura para compartilhamento de chaves.
    - **Desvantagem:** Pode ser mais lenta em comparação à criptografia simétrica.
3. **Criptografia de Hash:**
    - Produz um código único baseado nos dados, conhecido como **hash**, mas não é reversível.
    - **Exemplo:** SHA-256 (Secure Hash Algorithm).
    - **Usos comuns:** Verificação de integridade de dados e armazenamento seguro de senhas.

### **Por que a criptografia de dados é importante?**

- **Confidencialidade:** Garante que apenas destinatários autorizados possam acessar os dados.
- **Integridade:** Protege os dados contra alterações durante a transmissão ou armazenamento.
- **Autenticidade:** Ajuda a verificar a identidade do emissor ou do destinatário.
- **Conformidade:** Cumpre regulamentos de segurança, como o GDPR e LGPD.

### **Casos de uso da criptografia**

1. **Comunicações seguras:** Proteção de mensagens e e-mails (ex.: criptografia ponta a ponta em aplicativos como WhatsApp).
2. **Armazenamento de dados:** Proteção de arquivos sensíveis, como dados médicos ou financeiros.
3. **Transações online:** Segurança em compras na internet e operações bancárias.
4. **Autenticação:** Uso de certificados digitais para validar identidades.

### **Desafios da criptografia**

- **Gestão de chaves:** Proteger e distribuir chaves é crítico e pode ser desafiador.
- **Performance:** Criptografia forte pode ser mais lenta em sistemas com alta demanda.
- **Ataques avançados:** Algoritmos fracos ou mal implementados podem ser vulneráveis a ataques.



