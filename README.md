# BioConnect REST API to delete users

Base URL Staging: 
```
http://bioconnect.io:3000/v1
```

BioConnect API requires all requests to have a valid API key, specified in HTTP authorization header as
```
Authorization: TZ3SNerXmyEvyPOomoXWCAtt
```

## Delete many users
#### DELETE /users/delete?user_guids[]=:user_guid&user_guids[]=:user_guid...

Response Object Type: JSON

Response Object Schema
```javascript
{
  "status" : :status_code,
  "deleted_user_guids" : [ :user_guid, :user_guid ... ]
}
```

Response Parameters 
status : String 
- "success"
- "failure"

deleted_user_guids : Array of Strings

### Example: Delete many users
#### DELETE /users/delete?user_guids[]=e1e43705-761d-4ab0-b882-967ffb91bb4e&users_guids[]=f9a7a7b4-09a7-4b66-966f-0c80633b9112
Response
```javascript
{
  "status" : "success",
  "deleted_user_guids" : [ "e1e43705-761d-4ab0-b882-967ffb91bb4e", "f9a7a7b4-09a7-4b66-966f-0c80633b9112" ]
}
```

## Delete all users
#### DELETE /users/delete-all
Response Object Type: JSON

Response Object Schema
```javascript
{
  "status" : :status_code,
  "deleted_user_guids" : [ :user_guid, :user_guid ... ]
}
```

Response Parameters
status : String
- "success"
- "failure"

### Example: Delete all users
#### DELETE /users/delete-all
Response
```javascript
{
  "status" : "success",
  "deleted_user_guids" : [ "e1e43705-761d-4ab0-b882-967ffb91bb4e", "f9a7a7b4-09a7-4b66-966f-0c80633b9112" ... ]
}
```
