## nestjs-prisma-crud

NestJS + Prisma + Cloud Run + Cloud SQL

## Installation

```bash
$ yarn install
```

## Running the app

```bash
# development
$ docker-compose up -d
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```

## Test

```bash
# unit tests
$ yarn run test

# e2e tests
$ yarn run test:e2e

# test coverage
$ yarn run test:cov
```

## Deploy to Cloud Run

```bash
gcloud run deploy PROJECT_NAME \
 --source . \
 --project PROJECT_ID \
 --platform=managed \
 --region REGION \
 --allow-unauthenticated \
 --add-cloudsql-instances PROJECT_ID:REGION:NAME \
 --set-env-vars="DATABASE_URL=postgresql://postgres:password@localhost:5432/postgres?host=/cloudsql/PROJECT_ID:REGION:NAME"
```

## License

Nest is [MIT licensed](LICENSE).
