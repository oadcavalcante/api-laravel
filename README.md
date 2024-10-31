# API de Séries e Episódios em Laravel

Esta API permite gerenciar séries e episódios. Com ela, você pode listar, criar, atualizar e excluir séries, bem como listar episódios e fazer login na aplicação.

## Endpoints

### Séries

- **Listar todas as séries**  
  `GET /series`  
  Retorna uma lista com todas as séries cadastradas.

- **Listar episódios de uma série específica**  
  `GET /series/{series}/episodes`  
  Retorna todos os episódios da série especificada por `{series}`.

- **Criar uma nova série**  
  `POST /series`  
  Cria uma nova série com base nos dados fornecidos.

- **Atualizar uma série existente**  
  `PUT /series/{id}`  
  Atualiza todos os dados da série especificada por `{id}`.

- **Deletar uma série**  
  `DELETE /series/{id}`  
  Remove a série especificada por `{id}` do banco de dados.

### Episódios

- **Atualizar um episódio específico**  
  `PATCH /episodes/{episodes}`  
  Atualiza informações de um episódio específico, identificado por `{episodes}`.

### Autenticação

- **Login de usuário**  
  `POST /login`  
  Permite que o usuário faça login na aplicação para acessar endpoints protegidos.

---

## Requisitos e Instalação

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/api-series-episodios.git
   cd api-series-episodios
2. **Instalar dependências:**
   ```bash
   composer install
3. **Configurar o ambiente:**
   Renomeie o arquivo .env.example para .env e ajuste as configurações de banco de dados e outras variáveis de ambiente.
4. **Gerar chave da aplicação:**
   ```bash
   php artisan key:generate
5. **Iniciar o servidor:**
   ```bash
   php artisan serve

## Exemplo de Requisição
Para realizar uma requisição de exemplo para o endpoint de listagem de séries:
```bash
curl -x GET http://localhost:8000/series
