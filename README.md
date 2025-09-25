# Friends API com Autenticação JWT

## Descrição
Este projeto é uma **API RESTful** para gerenciar uma lista de amigos.  
A API permite registrar usuários, fazer login e realizar operações CRUD (Criar, Ler, Atualizar, Deletar) sobre amigos. Todos os endpoints de amigos são protegidos por **autenticação de usuário usando JWT e sessões**.

---

## Tecnologias
- Node.js
- Express
- JSON Web Token (JWT)
- Express-session

---

## Funcionalidades

### **Registro de usuário**
- **Endpoint:** `/register`  
- **Método:** POST  
- **Body (JSON):**
```json
{
  "username": "user2",
  "password": "password2"
}
{"message": "User successfully registered. Now you can login"}
Login de usuário
Endpoint: /login

Método: POST

Body (JSON):

json
Copiar código
{
  "username": "user2",
  "password": "password2"
}

Resposta: User successfully logged in

Cria um token JWT e uma sessão para acessar os endpoints protegidos.

Gerenciar amigos (/friends)
Todos os endpoints abaixo exigem que o usuário esteja logado.

Operação	Método	Endpoint	Body (JSON)	Descrição
Listar todos	GET	/friends	-	Retorna todos os amigos cadastrados
Buscar por email	GET	/friends/:email	-	Retorna os dados do amigo específico
Adicionar amigo	POST	/friends	{ "email": "", "firstName": "", "lastName": "", "DOB": "" }	Adiciona um novo amigo
Atualizar amigo	PUT	/friends/:email	{ "firstName": "", "lastName": "", "DOB": "" }	Atualiza os dados de um amigo existente
Deletar amigo	DELETE	/friends/:email	-	Remove um amigo pelo email

Como rodar a API
Clone o repositório:

bash
Copiar código
git clone https://github.com/Douglas-Pedroso/friends-api.git
cd friends-api
Instale as dependências:

bash
Copiar código
npm install
Inicie o servidor:

bash
Copiar código
npm start
O servidor rodará na porta 5000.
