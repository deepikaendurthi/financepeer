# Authentication

Given an `app.js` file and a database file `userData.db` consisting of a table `user`.

Write APIs to perform operations on the table `user` containing the following columns,

**User Table**

| Column   | Type |
| -------- | ---- |
| username | TEXT |
| name     | TEXT |
| password | TEXT |
| gender   | TEXT |
| location | TEXT |

### API 1

#### Path: `/register`

#### Method: `POST`

**Request**

```
{
  "username": "adam_richard",
  "name": "Adam Richard",
  "password": "richard_567",
  "gender": "male",
  "location": "Detroit"
}
```

- **Scenario 1**

  - **Description**:

    If the username already exists

  - **Response**
    - **Status code**
      ```
      400
      ```
    - **Status text**
      ```
      User already exists
      ```

- **Scenario 2**

  - **Description**:

    If the registrant provides a password with less than 5 characters

  - **Response**
    - **Status code**
      ```
      400
      ```
    - **Status text**
      ```
      Password is too short
      ```

- **Scenario 3**

  - **Description**:

    Successful registration of the registrant

  - **Response**
    - **Status code**
      ```
      200
      ```
    - **Status text**
    ```
    User created successfully
    ```

### API 2

#### Path: `/login`

#### Method: `POST`

**Request**

```
{
  "username": "deepika",
  "password": "endurthi@26"
}
```

- **Scenario 1**

  - **Description**:

    If an unregistered user tries to login

  - **Response**
    - **Status code**
      ```
      400
      ```
    - **Status text**
      ```
      Invalid user
      ```

- **Scenario 2**

  - **Description**:

    If the user provides incorrect password

  - **Response**
    - **Status code**
      ```
      400
      ```
    - **Status text**
      ```
      Invalid password
      ```

- **Scenario 3**

  - **Description**:

    Successful login of the user

  - **Response**

    - **Status code**
      ```
      200
      ```
    - **Status text**

      ```
      Login success!

      ```

<br/>

Use `npm install` to install the packages.

**Export the express instance using the default export syntax.**

**Use Common JS module syntax.**
