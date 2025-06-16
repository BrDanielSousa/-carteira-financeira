
# 💸 Carteira Virtual com Transações (Depósito, Transferência e Reversão)

Este projeto é uma aplicação web desenvolvida em Laravel que simula uma carteira financeira com suporte a três tipos de transações: depósito, transferência entre carteiras e reversão de transações.

---

## 🚀 Tecnologias Utilizadas

- PHP 8.x  
- Laravel 12  
- PostgreSQL  
- Docker (ambiente containerizado)  
- Blade (Template Engine)  
- Bootstrap (Interface)  

---

## ⚙️ Funcionalidades

- Cadastro de usuários  
- Criação automática de carteira para cada usuário  
- Depósito de valores  
- Transferência entre carteiras diferentes  
- Reversão de depósitos e transferências  
- Histórico detalhado das transações  
- Geração de comprovante com informações completas da transação  

---

## 🧾 Tipos de Transações

| Tipo            | Ação                                     |
|-----------------|------------------------------------------|
| `deposito`      | Adiciona saldo à carteira                |
| `transferencia` | Move saldo entre duas carteiras          |
| `reversao`      | Reverte um depósito ou transferência     |

---

## 📄 Como Rodar o Projeto

### 🐳 Usando Docker (Recomendado)

1. Clone o repositório:

\`\`\`bash
git clone https://github.com/seu-usuario/carteira-digital.git
cd carteira-digital
\`\`\`

2. Crie o arquivo \`.env\`:

\`\`\`bash
cp .env.example .env
\`\`\`

3. Configure as variáveis de ambiente no arquivo \`.env\`, por exemplo:

\`\`\`
DB_CONNECTION=pgsql
DB_HOST=postgres
DB_PORT=5432
DB_DATABASE=carteirafinanceira
DB_USERNAME=carteirauser
DB_PASSWORD=carteirapassword
\`\`\`

4. Suba os containers Docker:

\`\`\`bash
docker-compose up -d
\`\`\`

5. Instale as dependências PHP:

\`\`\`bash
docker-compose run --rm composer install
\`\`\`

6. Gere a chave da aplicação:

\`\`\`bash
docker-compose run --rm artisan key:generate
\`\`\`

7. Execute as migrações e seeders:

\`\`\`bash
docker-compose run --rm artisan migrate --seed
\`\`\`

8. Crie o link simbólico do storage:

\`\`\`bash
docker-compose run --rm artisan storage:link
\`\`\`

9. Ajuste permissões no storage:

\`\`\`bash
docker exec -it laravel-app chown -R www-data:www-data /var/www/storage
\`\`\`

10. Instale as dependências Node.js:

\`\`\`bash
docker-compose run --rm npm install
\`\`\`

11. Compile os assets:

\`\`\`bash
docker-compose run --rm npm run build
\`\`\`

---

### Instalação Manual (Sem Docker)

1. Clone o repositório:

\`\`\`bash
git clone https://github.com/seu-usuario/carteira-digital.git
cd carteira-digital
\`\`\`

2. Crie o arquivo \`.env\`:

\`\`\`bash
cp .env.example .env
\`\`\`

3. Instale as dependências PHP:

\`\`\`bash
composer install
\`\`\`

4. Gere a chave da aplicação:

\`\`\`bash
php artisan key:generate
\`\`\`

5. Execute as migrações e seeders:

\`\`\`bash
php artisan migrate --seed
\`\`\`

6. Inicie o servidor:

\`\`\`bash
php artisan serve
\`\`\`
