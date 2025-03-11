<h1>🛒 Backend - E-commerce</h1>

<p>Este é o backend do projeto E-commerce, desenvolvido com Node.js, Express e Stripe. Ele é responsável pela autenticação de usuários, gerenciamento de produtos, carrinho de compras e integração com o Stripe para processamento de pagamentos.</p>

<h2>🚀 Funcionalidades</h2>
✔️ API RESTful para gerenciamento de produtos e usuários 🛍️</br>
✔️ Autenticação de usuários via Firebase 🔐</br>
✔️ Integração com o Stripe para pagamentos 💳</br>
✔️ Persistência de dados com Firebase Realtime Database 📦</br>
✔️ Middleware para proteção de rotas privadas 🛡️</br>

<h2>🛠️ Tecnologias Utilizadas</h2>
Node.js - Ambiente de execução JavaScript no servidor</br>
Express.js - Framework para criação de APIs</br>
Firebase Authentication - Sistema de login e cadastro de usuários</br>
Firebase Realtime Database - Armazenamento de dados em tempo real</br>
Stripe API - Processamento de pagamentos online</br>
CORS - Gerenciamento de permissões de requisições</br>
dotenv - Gerenciamento de variáveis de ambiente</br>

<h2>📦 Instalação e Execução</h2>

<h3>🔧 Configuração do Projeto</h3>
--Clone o repositório do backend:--

```
sh
git clone https://github.com/seu-usuario/ecommerce-backend.git</br
```
--Acesse a pasta do backend:--
```
sh
cd backend
```
--Instale as dependências:--
```
sh
npm install
```
--Crie um arquivo .env na raiz do projeto e adicione as variáveis de ambiente:--
```
FRONT_END_URL=http://localhost:3000
STRIPE_SECRET_API_KEY=sua_chave_do_stripe
```
<h3>▶️ Executando o Servidor</h3>
Para iniciar o servidor backend, utilize:

```
sh
node app.js
```

  ou</br>

```
sh
npm start
```
O servidor será iniciado na porta 5005.</br>

<h2>📡 Rotas da API</h2>
<h3>🛒 Criar sessão de checkout</h3>
Endpoint:

```
POST /create-checkout-session</br>
```

Body (JSON):

```
{
  "products": [
    {
      "id": "6228f7a3b7e6cb904bbe0134",
      "name": "Vans Old Skool",
      "price": 350,
      "quantity": 1
    }
  ]
}
```

Resposta esperada:</br>

```
{
  "url": "https://checkout.stripe.com/pay/..."
}
```
O usuário será redirecionado para a página do Stripe para finalizar a compra.</br>
