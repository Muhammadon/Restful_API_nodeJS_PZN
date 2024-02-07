# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers :
- Authorization : Token

Request Body :

```json
{
    "first_name": "madun",
    "last_name": "sukse",
    "email": "madun@gmail.com",
    "phone": "085234456789"
}
```

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "first_name": "madun",
        "last_name": "sukse",
        "email": "madun@gmail.com",
        "phone": "085234456789"
    }
}
```

Response body Error :

```json
{
    "errors": "Email is not valid format"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Headers :
- Authorization : Token

Request Body :

```json
{
    "first_name": "madun",
    "last_name": "sukse",
    "email": "madun@gmail.com",
    "phone": "085234456789"
}
```

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "first_name": "madun",
        "last_name": "sukse",
        "email": "madun@gmail.com",
        "phone": "085234456789"
    }
}
```

Response body Error :

```json
{
    "errors": "Email alrleady used others  contact"
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Headers :
- Authorization : Token

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "first_name": "madun",
        "last_name": "sukse",
        "email": "madun@gmail.com",
        "phone": "085234456789"
    }
}
```

Response body Error :

```json
{
    "errors": "Contact is not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers :
- Authorization : Token

Query Params :
- name : Search by first_name or last_name, using like, optional
- email : Search by email using like, optional
- phone : Search by phone using like
- page : number of page, default 1
- size : size perpage, default 10

Response Body Success :

```json
{
    "data": [
        {
            "id": 1,
            "first_name": "madun",
            "last_name": "sukse",
            "email": "madun@gmail.com",
            "phone": "085234456789"
        },
        {
            "id": 2,
            "first_name": "madun",
            "last_name": "sukse",
            "email": "madun@gmail.com",
            "phone": "085234456789"
        }
    ],
    "paging": {
        "page": 1,
        "total_page": 3,
        "total_item": 30
    }
}
```

Response body Error :

```json
{
    "errors": "Email alrleady used others  contact"
}
```

## Remove Contact API

Endpoint : DELETE /api/contacts/:id

Headers :
- Authorization : Token

Response Body Success :

```json
{
    "data": "oke"
}
```

Response body Error :

```json
{
    "errors": "Contact is not found"
}
```