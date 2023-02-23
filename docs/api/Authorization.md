# That document describes API that is used by clients to interact with ProjectHub

### POST /api/v1/user/new
<details>
<summary>Registration</summary>

#### Request body:
```
{
	“email”:	string,
	“username”:	string,
	“password”:	string
}
```

#### Example:
```
curl --location --request POST 'https://cub.it/api/v1/user/new' \
--header 'Content-Type: application/json' \
--data-raw '{
	“email”: “template.email@gmail. com”,
	“username”: “Alex”,
	“password”: “Aa123456”
}'
```

#### Response:
HTTP status code: 200
```
{
	"token": "cabef633-3b34-45db-801f-d5b21b9e7bee",
	"userId": "21489"
}
```
</details>

### POST /api/v1/user/login
<details>
<summary>Authorization</summary>

#### Request body:
```
{
	“email”:	string,
	“password”:	string
}
```

#### Example:
	
```
curl --location --request POST 'https://cub.it/login' \
--header 'Content-Type: application/json' \
--data-raw '{
	“email”: “template.email@gmail.com”,
	“password”: “Aa123456”
}'
```

#### Response:
HTTP status code: 200
```
{
	"token": "cabef633-3b34-45db-801f-d5b21b9e7bee",
	"userId" : "21489"
}
```
</details>
