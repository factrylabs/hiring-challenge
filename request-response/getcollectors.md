# Succesful GET collectors request

## Request
```
curl -X GET \
   https://demo.factry.io/hiringchallenge/historian/collectors \
  -H 'Authorization: Bearer mysecretJWTtoken'
```

## Response code
`200 OK`

## Response headers
```
content-type: application/json; charset=UTF-8
server: Caddy
x-powered-by: Express
```

## Response body
```
[{
	"ID": "3f7f9ee0-869c-11e8-bc2e-df8e8887807d",
	"Name": "OPC-UA opclabs collector",
	"Description": "Gathers data from OPClabs OPC-UA demo server",
	"Type": "factry-opcua-collector",
	"Version": "0.1.0",
	"Status": "active",
	"SettingsSchema": {},
	"Settings": {
		"UAAuthentication": "anonymous",
		"UAEndpoint": "opc.tcp://opcuaserver.com:48010",
		"UAPassword": "",
		"UAUsername": ""
	},
	"MetricSettingsSchema": {},
	"CreatedBy": null,
	"CreatedAt": "2018-07-13T12:57:07.314Z",
	"UpdatedBy": null,
	"UpdatedAt": "2018-07-13T13:15:38.244Z",
	"Attributes": {}
}]
```

# Unsuccesful GET collectors request

## Request
```
curl -X GET \
   https://demo.factry.io/hiringchallenge/historian/collectors \
  -H 'Authorization: Bearer myfaultysecretJWTtoken'
```

## Response code
`401 Unauthorized`

## Response headers
```
content-type: application/json; charset=UTF-8
server: Caddy
x-powered-by: Express
```

## Response body
```
{
    "message":"code=401, message=Invalid or expired jwt, invalid character '\' looking for beginning of object key string"
}
```
