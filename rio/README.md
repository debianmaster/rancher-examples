
## Hasura on rio

```sh

rio run -p 5432/tcp --name=postgres2 postgres
rio run -p 8080/http -e HASURA_GRAPHQL_ADMIN_SECRET=supersecret -e HASURA_GRAPHQL_DATABASE_URL='postgres://postgres:@postgres2:5432/postgres' -e HASURA_GRAPHQL_ENABLE_CONSOLE="true" --name=hasura2 hasura/graphql-engine:pull2395-31a51dcd



```
