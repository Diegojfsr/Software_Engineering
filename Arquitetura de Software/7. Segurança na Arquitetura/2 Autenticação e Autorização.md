**Autenticação** e **autorização** são conceitos fundamentais na segurança de sistemas e redes, mas têm funções distintas. Vamos explorá-los:

### **O que é Autenticação?**

A autenticação é o processo de **verificar a identidade de um usuário ou sistema**. Basicamente, é o momento em que alguém prova quem realmente é.

#### **Como funciona?**

- O sistema solicita **credenciais** (ex.: nome de usuário e senha) para validar o acesso.
- Uma vez autenticado, o sistema reconhece o usuário.

#### **Exemplos de autenticação:**

1. **Senhas:** Entrada de um nome de usuário e senha.
2. **Autenticação de dois fatores (2FA):** Além da senha, solicita um código enviado ao celular ou e-mail.
3. **Biometria:** Impressão digital, reconhecimento facial ou de voz.
4. **Certificados digitais:** Verificação de identidade por meio de chaves criptográficas.

#### **Exemplo prático:**

No momento de login em um sistema, como ao acessar um e-mail, você fornece as credenciais e comprova sua identidade. Essa etapa é a autenticação.

### **O que é Autorização?**

A autorização ocorre após a autenticação e se refere ao processo de **determinar o que um usuário autenticado tem permissão para fazer** ou acessar no sistema.

#### **Como funciona?**

- O sistema verifica as **permissões** atribuídas ao usuário para conceder (ou negar) acesso a determinados recursos.

#### **Exemplos de autorização:**

1. **Acesso baseado em função:** Um administrador pode ter acesso total, enquanto um usuário comum pode acessar apenas certas áreas.
2. **Permissões em arquivos:** Determinar quem pode ler, editar ou excluir um documento.
3. **Controles de acesso em APIs:** Verificar se um usuário pode consumir certos endpoints.

#### **Exemplo prático:**

Após fazer login (autenticação), um funcionário acessa apenas os sistemas relacionados ao seu departamento, e não os administrativos. Isso é a autorização.

### **Diferença entre Autenticação e Autorização**

|**Aspecto**|**Autenticação**|**Autorização**|
|---|---|---|
|**Pergunta-chave**|Quem é você?|O que você pode fazer?|
|**Foco**|Verificar identidade|Conceder ou negar permissões|
|**Ocorrência**|Sempre antes da autorização|Ocorre após a autenticação|
|**Exemplo prático**|Inserir nome de usuário e senha|Acessar ou não relatórios financeiros|

### **Por que são importantes?**

- **Autenticação:** Impede que usuários não identificados acessem o sistema.
- **Autorização:** Evita o acesso indevido a informações ou funcionalidades sensíveis.
