# Fitur API Users

## User Register

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

## User Login

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

## User Info

### `GET /api/users/current`

Endpoint ini digunakan untuk mendapatkan info user yang sudah login.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/current`

- **Headers**
  Accept: application/json
  Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

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

## User Update

### `PATCH /api/users/current`

Endpoint ini digunakan untuk mendapatkan info user yang sudah login.

#### Request

- **URL**
  - `http://127.0.0.1:8000/api/users/current`

- **Headers**
  Accept: application/json
  Authorization: 814ddc14-11b0-46ed-962c-10a54e4c414e

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

