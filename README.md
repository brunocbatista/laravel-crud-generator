<h1 align="center">Gerar de CRUD's</h1>

<p align="center">
  Um gerador de CRUD's a partir de um comando baseado na arquitetura de actions. 
</p>

## Instruções de Uso

Siga as etapas abaixo para configurar e executar o projeto localmente.

### 1. Clonar o projeto

Clone este projeto em sua máquina local:

```bash
git clone https://github.com/brunocbatista/laravel-crud-generator.git
```

### 2. Pré-requisitos

Certifique-se de que você tenha o Docker e o Docker Compose configurados em sua máquina

### 3. Copie o arquivo .env.example para .env

```bash
cp .env.example .env
```
Certifique-se de que todas as credenciais no arquivo .env estejam configuradas corretamente.

### 4. Iniciar o Docker

Inicie o Docker usando o comando

```bash
docker compose up -d
```

### 5. Acessar o container

Acesse o container executando o seguinte comando

```bash
docker exec -it laravel-crud-generator-app bash
```

### 6. Instalar dependências do PHP

Dentro do container, instale as dependências do PHP usando o comando:

```bash
composer install
```

### 7. Executar configurações do laravel

Dentro do container, execute os comandos para gerar a chave do projeto e criar link da pasta storage com a pasta public:

```bash
php artisan key:generate
```

### 8. Executar migrations e seeders

Dentro do container, execute as migrations e seeders configurados usando o comando:

```bash
php artisan migrate --seed
```
