# API de Notas

API REST para gerenciamento de notas, desenvolvida com Node.js e Express. Os dados sao persistidos no arquivo `data.json`.

## Tecnologias

- Node.js
- Express 5
- Body Parser
- CORS
- Nodemon

## Funcionalidades

- Listar todas as notas
- Criar uma nota
- Atualizar uma nota
- Excluir uma nota

## Requisitos

- Node.js 18 ou superior
- npm

## Instalacao

```bash
npm install
```

## Execucao

Desenvolvimento, com reinicio automatico:

```bash
npm run dev
```

Execucao normal:

```bash
npm start
```

A API sera executada em `http://localhost:3000`.

## Endpoints

| Metodo | Rota | Descricao |
| --- | --- | --- |
| GET | `/api/notes` | Lista todas as notas |
| POST | `/api/notes` | Cria uma nota |
| PUT | `/api/notes/:id` | Atualiza uma nota |
| DELETE | `/api/notes/:id` | Exclui uma nota |

### Criar ou atualizar uma nota

Envie um JSON com os campos obrigatorios:

```json
{
  "titulo": "Comprar pao",
  "texto": "Passar na padaria depois da aula"
}
```

## Estrutura

```text
atividade-api-backend/
├── data.json          # Dados persistidos
├── server.js          # Configuracao, rotas e regras da API
├── package.json       # Scripts e dependencias
└── .gitignore         # Arquivos ignorados pelo Git
```

## Observacoes de producao

O `data.json` e adequado para fins didaticos e prototipos. Para producao, recomenda-se usar um banco de dados com autenticacao, validacao de dados, controle de concorrencia, backups e paginacao.

## Deploy

- No Render, configure:
  - **Build Command:** `npm install`
  - **Start Command:** `npm start`
  - **Root Directory:** deixe vazio quando o repositorio contiver somente o backend
- API publicada: [INSIRA O LINK DO DEPLOY]
- Repositorio: [INSIRA O LINK DO GITHUB]

> Nao use `node index.js`: o arquivo principal deste projeto e `server.js`.
