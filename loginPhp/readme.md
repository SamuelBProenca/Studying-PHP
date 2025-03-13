### **Descrição do Projeto**
Crie um sistema de login funcional utilizando PHP e MySQL. O sistema deve permitir o registro de novos usuários, autenticação e armazenamento seguro das senhas.

---

### **Tarefas**

#### **1. Configuração Inicial**
1. Configure um servidor local (ex.: XAMPP, WAMP ou Laragon).
2. Crie um banco de dados chamado `sistema_login`.
3. Adicione uma tabela `usuarios` com as seguintes colunas:
   - `id` (INT, chave primária, auto increment).
   - `email` (VARCHAR, único).
   - `senha` (VARCHAR, para a senha hash).

---

#### **2. Registro de Usuários**
1. Crie uma página `register.php`:
   - Inclua um formulário com campos para e-mail e senha.
   - Valide os dados do usuário (e-mail válido e senha obrigatória).
2. No backend:
   - Certifique-se de que o e-mail ainda não está cadastrado.
   - Use `password_hash` para armazenar a senha de forma segura.
   - Insira o usuário no banco de dados.
3. Exiba mensagens apropriadas em caso de erros (e-mail duplicado, dados inválidos).

---

#### **3. Login de Usuários**
1. Crie uma página `login.php`:
   - Inclua um formulário com campos para e-mail e senha.
2. No backend:
   - Verifique se o e-mail existe no banco de dados.
   - Use `password_verify` para comparar a senha digitada com a senha hash armazenada.
   - Configure uma sessão PHP para autenticar o usuário após o login.
3. Redirecione o usuário para uma página de dashboard ao fazer login.

---

#### **4. Página de Dashboard**
1. Crie uma página `dashboard.php`:
   - Somente usuários logados devem ter acesso.
   - Exiba uma mensagem de boas-vindas com o e-mail do usuário autenticado.
2. Adicione um botão para "Logout":
   - Destrua a sessão ao clicar para finalizar a autenticação.

---

#### **5. Segurança**
1. Proteja todas as páginas privadas:
   - Verifique se o usuário está autenticado (sessão válida).
2. Evite ataques de SQL Injection usando **Prepared Statements** em todas as queries.
3. Configure o código para escapar dados de entrada (ex.: `htmlspecialchars()`).

---

### **README.md**
Adicione ao README:
- **Título**: Sistema de Login em PHP e MySQL.
- **Descrição**: Um sistema seguro para autenticação de usuários.
- **Requisitos**:
  - PHP 7.4+.
  - MySQL 5.7+.
  - Servidor local configurado.
- **Passos para Instalação**:
  1. Clone o repositório.
  2. Configure o banco de dados (instruções em `db.sql`).
  3. Atualize o arquivo `config.php` com as credenciais do banco.
- **Funcionalidades**:
  - Registro de novos usuários.
  - Login com autenticação segura.
  - Dashboard acessível apenas para usuários autenticados.

---
