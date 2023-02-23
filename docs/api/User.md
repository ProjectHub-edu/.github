# That document describes API that is used by clients to interact with ProjectHub

### GET /api/v1/user/:userId
<details>
<summary>All groups that user take part in</summary>
	
#### Example:
	
```
curl --location --request GET 'https://project-hub.herokuapp.com/api/v1/user/78988' \
--header 'Content-Type: application/json'
```
	
#### Response:
HTTP status code: 200
```
{
  "userName": "Alex",
  "email": "alex@gmail.com",
  "avatar_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
  "description": "Cool developer for your project ;)",
  "own_projects": [
    {
      "id": "93583",
      "title": "Tetris",
      "role_description": "Front-end developer"
    }
  ],
  "joined_projects": [
    {
      "id": "87987",
      "title": "ProjectHub",
      "role_description": "Front-end developer"
    },
    {
      "id": "65822",
      "title": "CubIT",
      "role_description": "Back-end developer"
    }
  ]
}
```
</details>
