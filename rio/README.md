
## Hasura on rio

```sh

rio run -p 5432/tcp --name=hasura hasura/graphql-engine:v1.0.0-beta.3

rio run -p 8080/http -e HASURA_GRAPHQL_ADMIN_SECRET=supersecret -e HASURA_GRAPHQL_DATABASE_URL='postgres://postgres:@postgres:5432/postgres' -e HASURA_GRAPHQL_ENABLE_CONSOLE="true" --name=hasura hasura/graphql-engine:v1.0.0-beta.3
default/hasura:v0
```
