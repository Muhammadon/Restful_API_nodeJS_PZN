# Adress API Spec

## Create Adress API

Endpoint : POST /api/contacts/:contactId/adresses

Headers :
- Authorization : token

Request Body :

```json
{
    "street": "jalan apa",
    "city": "kota apa",
    "province": "provinsi apa",
    "country": "negara apa",
    "postal_code": "kode pos"
}
```

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "street": "jalan apa",
        "city": "kota apa",
        "province": "provinsi apa",
        "country": "negara apa",
        "postal_code": "kode pos"
    }
}
```

Response Body Error :

```json
{
    "errors": "Country is required"
}
```

## Update Adress API

Endpoint : PUT /api/contacts/:contactId/adresses/:adressesId

Headers :
- Authorization : token

Request Body :

```json
{
    "street": "jalan apa",
    "city": "kota apa",
    "province": "provinsi apa",
    "country": "negara apa",
    "postal_code": "kode pos"
}
```

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "street": "jalan apa",
        "city": "kota apa",
        "province": "provinsi apa",
        "country": "negara apa",
        "postal_code": "kode pos"
    }
}
```

Response Body Error :

```json
{
    "errors": "Country is required"
}
```

## Get Adress API

Endpoint : GET /api/contacts/:contactId/adresses/:adressesId

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data": {
        "id": 1,
        "street": "jalan apa",
        "city": "kota apa",
        "province": "provinsi apa",
        "country": "negara apa",
        "postal_code": "kode pos"
    }
}
```

Response Body Error :

```json
{
    "errors": "Contact is not found"
}
```

## List Adress API

Endpoint : GET /api/contacts/:contactId/adresses

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data": [
        {
        "id": 1,
        "street": "jalan apa",
        "city": "kota apa",
        "province": "provinsi apa",
        "country": "negara apa",
        "postal_code": "kode pos"
        },
        {
        "id": 2,
        "street": "jalan apa",
        "city": "kota apa",
        "province": "provinsi apa",
        "country": "negara apa",
        "postal_code": "kode pos"
        },
    ]
}
```

Response Body Error :

```json
{
    "errors": "Contact is not found"
}
```

## Remove Adress API

Endpoint : GET /api/contacts/:contactId/adresses/:adressesId

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data": "oke"
}
```

Response Body Error :

```json
{
    "errors": "Adress is not found"
}
```