# That document describes API that is used by clients to interact with ProjectHub

### GET /api/v1/projects
<details>
<summary>Get all projects</summary>

#### Example:
	
```
curl --location --request GET 'https://project-hub.herokuapp.com/api/v1/projects' \
--header 'Content-Type: application/json'
```
	
#### Response:
HTTP status code: 200
```
{
	"projects": [
		{
			"id": 1,
			"title": "project 1",
			"description": "description 1",
			"status": "IN_PROGRESS",
			"image_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
		},
		{
			"id": 2,
			"title": "project 2",
			"description": "description 2",
			"status": "OPEN",
			"image_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
			"available_roles": ["role1", "role2", "role3"]
		}
	]
}
```
</details>

### POST /api/v1/projects/new
<details>
<summary>Create new project</summary>

#### Request body:
```
{
	"title": string,
	"description": string,
	"my_role": string
}
```

#### Example:
```
curl --location --request POST 'https://cub.it/api/v1/user/new' \
--header 'Content-Type: application/json' \
--data-raw '{
  "title": "ProjectHub",
  "description": "Supper cool project idea!",
  "my_role": "Front-end developer"
}'
```

#### Response:
HTTP status code: 200
```
{
  "project_id": "789982"
}
```
</details>

### GET /api/v1/projects/:project_id
<details>
<summary>Get detailed information about a project</summary>

#### Example:
	
```
curl --location --request GET 'https://project-hub.herokuapp.com/api/v1/projects/98567' \
--header 'Content-Type: application/json'
```
	
#### Response:
HTTP status code: 200
```
{
  "id": 98567,
  "title": "project 1",
  "description": "project 1",
  "status": "IN_PROGRESS",
  "project_img_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
  "created_date": "2023-02-23T09:32:13.785+00:00",
  "roles": [
    {
      "role_name": "Front-end",
      "description": "Work on React application",
      "user": {
        "id": 17887,
        "image_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
        "name": "Alex"
      }
    },
    {
      "role_name": "Back-end",
      "description": "Work on Spring application",
      "user": {
        "id": 78991,
        "image_url": "https://schemazone.com/wp-content/uploads/2021/03/Project-Manager.jpg",
        "name": "John"
      }
    }
  ]
}
```
</details>
