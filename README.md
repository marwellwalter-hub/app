# White Bull / Kings - Sales Force MVP

Monorepo com backend (NestJS + Prisma) e app mobile (Expo RN).

## Estrutura

- `backend/`: API NestJS + Prisma
- `mobile/`: App Expo (offline-first)

## Requisitos

- Node.js 20+
- Docker + Docker Compose

## Setup local (backend + postgres)

```bash
docker-compose up --build
```

## Variáveis de ambiente

Backend usa:

- `DATABASE_URL` (Postgres)
- `PORT`
- `BLING_CLIENT_ID`
- `BLING_CLIENT_SECRET`
- `BLING_REDIRECT_URI`
- `BLING_SCOPES`
- `BLING_BASE_URL` (ex.: https://www.bling.com.br/Api/v3)

## Swagger

Acesse `http://localhost:3000/docs`.

## Prisma

```bash
cd backend
npm install
npm run prisma:generate
npm run prisma:migrate
```

## Notas de Integração Bling

- Tokens OAuth2 serão armazenados apenas no backend (criptografados).
- O backend fará refresh automático do token.
- Mapeamentos idempotentes serão guardados em `bling_mappings`.
