# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
    "username": "madun",
    "password":"123456",
    "name": "dynamic_M"
}
```

Response Body Success :

```json
{
    "data": {
        "username": "madun",
        "name": "dynamic_M"
    }
}
```

Response Body Error :

```json
{
    "error": "Username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username": "madun",
    "password": "123456"
}
```

Response Body Success :

```json
{
    "data": {
        "token": "unique-token"
    }
}
```

Response Body Error :

```json
{
    "error": "Invalid username or password"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :
- Authorization: token

Request Body :

```json
{
    "name": "new name", // optional
    "password": "new password" // optional
}
```

Response Body Success :

```json
{
    "data": {
        "username": "madun",
        "name": "new name",
    }
}
```

Response Body Error :

```json
{
    "errors": "Name length max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :
- Authorization: token

Response Body Success :

```json
{
    "data": {
        "username": "madun",
        "name": "dynamic_M",
    }
}
```

Response Body Error :

```json
{
    "errors": "Unauthorized"
}
```

## Logout User API

Endpoin : DELETE /api/users/logout

Headers :
- Authorization: token

Response Body Success :

```json
{
    "data": "oke"
}
```

Response Body Error :

```json
{
    "error": "Unauthorized"
}
```