# d1-secret-rest
Fetch results or execute queries against a D1 CRUD REST API

## Get rows from table
```curl
curl --location 'https://d1-rest.<YOUR-IDENTIFIER>.workers.dev/rest/users?limit=2' \
--header 'Authorization: Bearer <YOUR-SECRET-VALUE>'
```

## Raw SQL
```curl
curl --location 'https://d1-rest.<YOUR-IDENTIFIER>.workers.dev/query' \
--header 'Authorization: Bearer <YOUR-SECRET-VALUE>' \
--header 'Content-Type: application/javascript' \
--data '{
    "query": "SELECT * FROM users LIMIT ?;",
    "params": [1]
}'
```