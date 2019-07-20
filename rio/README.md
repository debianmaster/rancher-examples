
## Hasura on rio

```sh

rio run -p 5432/tcp --name=postgres2 postgres
rio run -p 8080/http -e HASURA_GRAPHQL_ADMIN_SECRET=supersecret -e HASURA_GRAPHQL_DATABASE_URL='postgres://postgres:@postgres2:5432/postgres' -e HASURA_GRAPHQL_ENABLE_CONSOLE="true" --name=hasura2 hasura/graphql-engine:pull2395-31a51dcd

```


```sh
rio run -p 443/http --name=drone \
-e DRONE_KUBERNETES_ENABLED=true \
-e DRONE_KUBERNETES_NAMESPACE=default \
-e DRONE_SERVER_HOST=drone.cloud.run9.io \
-e DRONE_GITHUB_SERVER=https://github.com \
-e DRONE_GITHUB_CLIENT_ID=edummydummy5c8c \
-e DRONE_GITHUB_CLIENT_SECRET=791512dummydummydummyc47567e4 \
-e DRONE_RPC_SECRET=bea26a2221fd8090ea38720fc445eca6 \
-e DRONE_SERVER_PROTO=https drone/drone:1.0.0
```

## Code server

```sh
rio run -p 8443/http --name=code codercom/code-server --allow-http --no-auth
```
