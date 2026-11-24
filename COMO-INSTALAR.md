# Como instalar e executar o projeto

## Requisitos

- Node.js 22.13 ou versão mais recente.
- Navegador web atual.
- Git para obter o repositório.

Não é necessário instalar Docker ou um servidor de banco de dados separado.

## Instalação

Abra dois terminais na raiz do repositório.

### Terminal 1 - API

```bat
cd codigo-fonte\backend
npm install
npm run seed
npm run dev
```

A API ficará disponível em `http://localhost:3000`.

### Terminal 2 - interface

```bat
cd codigo-fonte\frontend
npm install
npm run dev
```

A interface ficará disponível em `http://localhost:5173`.

## Login de teste

- Usuário: `admin@doces.com`
- Senha: `admin123`

## Executar a aplicação integrada

```bat
cd codigo-fonte\frontend
npm run build
cd ..\backend
npm start
```

Depois, abra `http://localhost:3000`.

## Executar os testes

```bat
cd codigo-fonte\backend
npm test
```
