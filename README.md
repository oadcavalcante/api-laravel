<div align="center">

🐘

# API Laravel

**API REST em Laravel para gerenciar séries, temporadas, episódios e autenticação de usuários.**

<br />

[![Repositório público](https://img.shields.io/badge/repo-público-2ea44f?style=flat-square&logo=github&logoColor=white)](https://github.com/oadcavalcante/api-laravel)

<br />

[![PHP 8.1](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logoColor=fff&logo=php)](https://github.com/oadcavalcante/api-laravel) [![Laravel 9](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logoColor=fff&logo=laravel)](https://github.com/oadcavalcante/api-laravel) [![Laravel Sanctum](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logoColor=fff&logo=laravel)](https://github.com/oadcavalcante/api-laravel) [![PHPUnit](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logoColor=fff&logo=php)](https://github.com/oadcavalcante/api-laravel) [![Laravel Breeze](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logoColor=fff&logo=laravel)](https://github.com/oadcavalcante/api-laravel)

[![Guzzle](https://img.shields.io/badge/Guzzle-555555?style=flat-square)](https://github.com/oadcavalcante/api-laravel)

<br />

[Stack completa ↓](#stack)

<br />

[Documentação](https://github.com/oadcavalcante/api-laravel/blob/main/README.md) · [Deploy](#deploy) · [API](http://localhost:8000/api) · [Issues](https://github.com/oadcavalcante/api-laravel/issues)

</div>

## Features

- ✨ CRUD de séries protegido por autenticação Sanctum
- 🚀 Listagem de temporadas e episódios por série
- ⚡ Atualização de status de episódios assistidos
- 🎯 Endpoint de login com geração de token
- 🔧 Rotas web com autenticação Breeze
- 📦 Migrations e seeders para banco de dados

## Getting Started

| Ambiente | Comando / Link |
|----------|----------------|
| Primeira vez | `composer install && php artisan key:generate && php artisan serve` |
| Documentação | [README](https://github.com/oadcavalcante/api-laravel/blob/main/README.md) |
| Produção | N/A |

## Stack

- **Backend:** PHP 8.1, Laravel 9, Laravel Sanctum, PHPUnit, Laravel Breeze
- **Outros:** Guzzle

---

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
   ```

2. **Instalar dependências:**
   ```bash
   composer install
   ```

3. **Configurar o ambiente:**  
   Renomeie o arquivo `.env.example` para `.env` e ajuste as configurações de banco de dados e outras variáveis de ambiente.

4. **Gerar chave da aplicação:**
   ```bash
   php artisan key:generate
   ```

5. **Iniciar o servidor:**
   ```bash
   php artisan serve
   ```

## Exemplo de Requisição

Para realizar uma requisição de exemplo para o endpoint de listagem de séries:

```bash
curl -X GET http://localhost:8000/series
```
