# Succesful POST collectors request

## Request
```
curl -X POST \
   https://demo.factry.io/hiringchallenge/historian/collectors \
  -H 'Authorization: Bearer mytoken \
  -H 'Content-Type: application/json' \
  -d '{"Name":"NewCollector","Description":"NewDescription"}'
```
## Response code
`201 Created`

## Response headers
```
content-length: 20
content-type: application/json; charset=UTF-8
location: /collectorruntime/2ff60680-0bd4-11ea-b1c9-7b1e9281ce6e
server: Caddy
status: 201
x-powered-by: Express
```

## Response body
```
"Collector created."
```

# Unsuccesful POST collectors request

## Request
```
curl -X POST \
   https://demo.factry.io/hiringchallenge/historian/collectors \
  -H 'Authorization: Bearer myfaultytoken \
  -H 'Content-Type: application/json' \
  -d '{"Name":"NewCollector","Description":"NewDescription"}'
```
## Response code
`401 Unauthorized`

## Response headers
```
content-type: application/json; charset=UTF-8
server: Caddy
x-powered-by: Express
content-length: 101
```

## Response body
```
{
    "message": "code=401, message=Invalid or expired jwt, invalid character '\\b' in string escape code"
}
```
