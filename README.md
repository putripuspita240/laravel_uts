# 1. Fitur API Users

## A. User Register

### `POST /api/users`

Endpoint ini digunakan untuk register user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users`

- **Body**
  ```json
  {
      "username": "putripus",
      "password": "password123",
      "name": "Putri Puspitasari"
  }

## B. User Login

### `POST /api/users/login`

Endpoint ini digunakan untuk login user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/login`

- **Body**
  ```json
  {
      "username": "putripus",
      "password": "password123"
  }

- **Response**
  ```json
  {
    "data": {
        "id": 1,
        "username": "putripus",
        "name": "Putri",
        "token": "814ddc14-11b0-46ed-962c-10a54e4c414e"
    }
  }

## C. User Info

### `GET /api/users/current`

Endpoint ini digunakan untuk mendapatkan info user yang sudah login.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/current`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": {
        "id": 1,
        "username": "putripus",
        "name": "Putri",
        "token": "814ddc14-11b0-46ed-962c-10a54e4c414e"
    }
  }

## D. Update User

### `PATCH /api/users/current`

Endpoint ini digunakan untuk update user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/current`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Body**
  ```json
  {
    "name": "Putri"
  }

- **Response**
  ```json
  {
    "data": {
        "id": 1,
        "username": "putripus",
        "name": "Putri",
        "token": "814ddc14-11b0-46ed-962c-10a54e4c414e"
    }
  }

## E. User Logout

### `DELETE /api/users/logout`

Endpoint ini digunakan untuk logout user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/logout`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": true
  }

# 2. Fitur API Contacts

## A. Create Contact

### `POST /api/contacts`

Endpoint ini digunakan untuk create contact.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Body**
  ```json
  {
    "first_name": "Reiznu",
    "last_name": "Tjandrida",
    "email": "r.tjandrida@gmail.com",
    "phone": "085231565787"
  }

## B. Get Contact

### `GET /api/contacts/1`

Endpoint ini digunakan untuk mendapatkan data contact berdasarkan id.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "first_name": "Reiznu",
    "last_name": "Tjandrida",
    "email": "r.tjandrida@gmail.com",
    "phone": "085231565787"
  }

## C. Update Contact

### `PUT /api/contacts/1`

Endpoint ini digunakan untuk update contact.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Body**
  ```json
  {
    "first_name": "Reiznu Ahmad"
  }

- **Response**
  ```json
  {
    "first_name": "Reiznu Ahmad",
    "last_name": "Tjandrida",
    "email": "r.tjandrida@gmail.com",
    "phone": "085231565787"
  }

## D. Delete Contact

### `PATCH /api/contacts/1`

Endpoint ini digunakan untuk delete user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": true
  }

## E. Search Contact

### `GET /api/contacts`

Endpoint ini digunakan untuk melihat list seluruh contact.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/logout`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": [
        {
            "id": 1,
            "first_name": "Reiznu Ahmad",
            "last_name": "Tjandrida",
            "email": "r.tjandrida@gmail.com",
            "phone": "085231565787"
        },
        {
            "id": 2,
            "first_name": "Achmad",
            "last_name": "Bobi",
            "email": "bob@gmail.com",
            "phone": "085231565887"
        }
    ],
    "links": {
        "first": "http://127.0.0.1:8000/api/contacts?page=1",
        "last": "http://127.0.0.1:8000/api/contacts?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
            {
                "url": null,
                "label": "&laquo; Previous",
                "active": false
            },
            {
                "url": "http://127.0.0.1:8000/api/contacts?page=1",
                "label": "1",
                "active": true
            },
            {
                "url": null,
                "label": "Next &raquo;",
                "active": false
            }
        ],
        "path": "http://127.0.0.1:8000/api/contacts",
        "per_page": 10,
        "to": 2,
        "total": 2
    }
  }

# 3. Fitur API Address

## A. Create Address

### `POST /api/contacts/1/addresses`

Endpoint ini digunakan untuk create address.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1/addresses`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Body**
  ```json
  {
    "street": "Jl Abdurachman No 1 Alas Tipis Pabean Sidoarjo",
    "city": "Sidoarjo",
    "province": "Jawa Timur",
    "country": "Indonesia",
    "postal_code": "61253"
  }

## B. Get Address

### `GET /api/contacts/1/addresses/1`

Endpoint ini digunakan untuk mendapatkan data address berdasarkan id yang memiliki relasi dengan user.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1/addresess/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "street": "Jl Abdurachman No 1 Alas Tipis Pabean Sidoarjo",
    "city": "Sidoarjo",
    "province": "Jawa Timur",
    "country": "Indonesia",
    "postal_code": "61253"
  }

## C. Update Address

### `PUT /api/contacts/1/addresses/1`

Endpoint ini digunakan untuk update address.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1/addresses/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Body**
  ```json
  {
    "province": "Jatim"
  }

- **Response**
  ```json
  {
    "street": "Jl Abdurachman No 1 Alas Tipis Pabean Sidoarjo",
    "city": "Sidoarjo",
    "province": "Jatim",
    "country": "Indonesia",
    "postal_code": "61253"
  }

## D. Delete Address

### `PATCH /api/contacts/1/addresses/1`

Endpoint ini digunakan untuk delete address.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1/addresses/1`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": true
  }

## E. Search Address

### `GET /api/contacts/1/addresses`

Endpoint ini digunakan untuk melihat list seluruh address.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/contacts/1/addresses`

- **Headers**
  - Accept: application/json
  - Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

- **Response**
  ```json
  {
    "data": [
        {
            "id": 1,
            "street": "Jl Abdurachman No 1 Alas Tipis Pabean Sidoarjo",
            "city": "Sidoarjo",
            "province": "Jawa Timur",
            "country": "Indonesia",
            "postal_code": "61253"
        }
    ]
  }
