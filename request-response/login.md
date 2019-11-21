# Succesful login request

## Request
```
curl -X POST \
   https://demo.factry.io/hiringchallenge/auth/login \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'username=USERNAME&password=PASSWORD'
```

## Response code
`200 OK`

## Response headers
```
access-control-allow-origin: *
content-length: 228
content-type: text/plain; charset=UTF-8
server: Caddy
status: 200
vary: Origin
x-powered-by: Express
```

## Response body
```
mysecrettoken
```

# Unsuccessful login request

## Request
```
curl -X POST \
   https://demo.factry.io/hiringchallenge/auth/login \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'username=USERNAME&password=WRONGPASSWORD'
```

## Response code
`401 Unauthorized`

## Response headers
```
access-control-allow-origin: *
content-type: application/json; charset=UTF-8
server: Caddy
vary: Origin
x-powered-by: Express
content-length: 42
```

## Response body
```
{
    "message": "invalid username or password"
}
```
