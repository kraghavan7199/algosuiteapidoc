# AlgoSuite API Documentation

## Table of Contents
- [Authentication](#authentication)
  - [Register User](#register-user)
  - [Login User](#login-user)
  - [Get User Profile](#get-user-profile)
- [String Operations](#string-operations)
  - [Get Substring Data](#get-substring-data)
  - [Get String History](#get-string-history)
  - [Get String Suggestions](#get-string-suggestions)
- [Tree Operations](#tree-operations)
  - [Generate Binary Tree](#generate-binary-tree)
  - [Save Binary Tree](#save-binary-tree)
  - [Get Binary Tree Calculations](#get-binary-tree-calculations)
  - [Get User Tree](#get-user-tree)

## Authentication

### Register User
Register a new user account.

**Endpoint:** `POST /auth/register`

**Headers:**
```
Content-Type: application/json
```

**Request Body Schema:**
```json
{
    "name": "string",
    "email": "string",
    "password": "string"
}
```

**Response Schema:** `200 OK`
```json
{
    "token": "string"
}
```

### Login User
Authenticate an existing user.

**Endpoint:** `POST /auth/login`

**Headers:**
```
Content-Type: application/json
```

**Request Body Schema:**
```json
{
    "email": "string",
    "password": "string"
}
```

**Response Schema:** `200 OK`
```json
{
    "token": "string"
}
```

### Get User Profile
Retrieve the authenticated user's profile.

**Endpoint:** `GET /auth/user`

**Headers:**
```
auth-key: string
```

**Response Schema:** `200 OK`
```json
{
    "userId": "number",
    "email": "string",
    "name": "string"
}
```

## String Operations

### Get Substring Data
Get all possible substrings and related data for a given input string.

**Endpoint:** `GET /string/{inputstring}/substrings`

**Headers:**
```
auth-key: string
```

**Response Schema:** `200 OK`
```json
{
    "string": "string",
    "longestSubstringLength": "number",
    "uniqueSubstring": ["string"],
    "userId": "number"
}
```

### Get String History
Retrieve history of string operations with pagination.

**Endpoint:** `GET /string/history`

**Headers:**
```
auth-key: string
```

**Query Parameters Schema:**
```
criteria={"limit": "number", "skip": "number"}
```

**Response Schema:** `200 OK`
```json
[
    {
        "id": "number",
        "user_id": "number",
        "input_string": "string",
        "longest_substring_length": "number",
        "unique_substrings": ["string"],
        "created_at": "string (ISO date)"
    }
]
```

### Get String Suggestions
Get suggestions based on a search key.

**Endpoint:** `GET /string/{searchkey}/suggestions`

**Headers:**
```
auth-key: string
```

**Response Schema:** `200 OK`
```json
[
    "string"
]
```

## Tree Operations

### Generate Binary Tree
Generate a new binary tree with specified depth.

**Endpoint:** `POST /tree/generate`

**Headers:**
```
Content-Type: application/json
auth-key: string
```

**Request Body Schema:**
```json
{
    "depth": "number"
}
```

**Response Schema:** `200 OK`
```json
{
    "value": "number",
    "uniqueId": "string",
    "left": {
        "value": "number",
        "uniqueId": "string",
        "left": "object (recursive tree structure)",
        "right": "object (recursive tree structure)"
    },
    "right": {
        "value": "number",
        "uniqueId": "string",
        "left": "object (recursive tree structure)",
        "right": "object (recursive tree structure)"
    }
}
```

### Save Binary Tree
Save a binary tree structure.

**Endpoint:** `POST /tree`

**Headers:**
```
Content-Type: application/json
auth-key: string
```

**Request Body Schema:**
```json
{
    "tree": {
        "value": "number",
        "left": "object (recursive tree structure)",
        "right": "object (recursive tree structure)"
    }
}
```

**Response Schema:** `200 OK`
```json
"boolean"
```

### Get Binary Tree Calculations
Get calculations for the saved binary tree.

**Endpoint:** `GET /tree/`

**Headers:**
```
auth-key: string
```

**Response Schema:** `200 OK`
```json
{
    "sum": "number",
    "path": ["string"]
}
```

### Get User Tree
Retrieve the user's saved binary tree with calculations.

**Endpoint:** `GET /tree`

**Headers:**
```
auth-key: string
```

**Response Schema:** `200 OK`
```json
{
    "tree": {
        "value": "number",
        "uniqueId": "string",
        "left": "object (recursive tree structure)",
        "right": "object (recursive tree structure)"
    },
    "userId": "number",
    "maxSumPath": {
        "maxLeafToNode": {
            "sum": "number",
            "path": ["string"]
        }
    }
}
```
