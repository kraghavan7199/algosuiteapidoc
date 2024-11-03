# AlgoSuite APIs
# 📁 Folder: Auth 


## End-point: Register User
### Method: POST
>```
>/auth/register
>```
### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{
    "name": "Test User",
    "email": "",
    "password": "Password123!"
}
```

### Response: 200
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjIzLCJpYXQiOjE3MzA1NzE4NzYsImV4cCI6MTczMTE3NjY3Nn0.Q-fK2pYMMExY6kudOh8Dthw0I86CwSVur_BzOHVD6Hg"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Login User
### Method: POST
>```
>/auth/login
>```
### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{
    "email": "",
    "password": "Password123!"
}
```

### Response: 200
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjIzLCJpYXQiOjE3MzA1NzE5MzgsImV4cCI6MTczMTE3NjczOH0.8avu6lEyqd4W82c8xUAzaaGJ9iVxpJreFAhA2380z5g"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get User Profile
### Method: GET
>```
>/auth/user
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Response: 200
```json
{
    "userId": 23,
    "email": "testuser@example.com",
    "name": "Test User"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: String Operations 


## End-point: Get Substring Data
### Method: GET
>```
>/string//substrings
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Response: 200
```json
{
    "string": "calculation",
    "longestSubstringLength": 8,
    "uniqueSubstring": [
        "c",
        "ca",
        "cal",
        "a",
        "al",
        "alc",
        "alcu",
        "l",
        "lc",
        "lcu",
        "c",
        "cu",
        "cul",
        "cula",
        "culat",
        "culati",
        "culatio",
        "culation",
        "u",
        "ul",
        "ula",
        "ulat",
        "ulati",
        "ulatio",
        "ulation",
        "l",
        "la",
        "lat",
        "lati",
        "latio",
        "lation",
        "a",
        "at",
        "ati",
        "atio",
        "ation",
        "t",
        "ti",
        "tio",
        "tion",
        "i",
        "io",
        "ion",
        "o",
        "on",
        "n"
    ],
    "userId": 23
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get String History
### Method: GET
>```
>/string/history?criteria={"limit":10,"skip":0}
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Query Params

|Param|value|
|---|---|
|criteria|{"limit":10,"skip":0}|


### Response: 200
```json
[
    {
        "id": 37,
        "user_id": 23,
        "input_string": "teststring",
        "longest_substring_length": 6,
        "unique_substrings": [
            "t",
            "te",
            "tes",
            "e",
            "es",
            "est",
            "s",
            "st",
            "t",
            "ts",
            "s",
            "st",
            "str",
            "stri",
            "strin",
            "string",
            "t",
            "tr",
            "tri",
            "trin",
            "tring",
            "r",
            "ri",
            "rin",
            "ring",
            "i",
            "in",
            "ing",
            "n",
            "ng",
            "g"
        ],
        "created_at": "2024-11-02T18:26:24.755Z"
    }
]
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get String Suggestions
### Method: GET
>```
>/string//suggestions
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Response: 200
```json
[
    "testify",
    "testimony",
    "testing"
]
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
# 📁 Folder: Tree Operations 


## End-point: Generate Binary Tree
### Method: POST
>```
>/tree/generate
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{
    "depth": 3
}
```

### Response: 200
```json
{
    "value": 90,
    "uniqueId": "8c969ebb-a47f-4134-9d9e-584558f1d9ed",
    "left": {
        "value": 12,
        "uniqueId": "d1530347-d7a7-4884-9e8a-d93e3dffd027",
        "left": {
            "value": 76,
            "uniqueId": "557ddaf1-6c05-46f6-933b-e21bb15f812f"
        }
    },
    "right": {
        "value": 53,
        "uniqueId": "f7d8cbcc-b337-4105-8cbf-861cee301ce8",
        "right": {
            "value": 38,
            "uniqueId": "85401bfd-3aec-42e0-bebe-fa593d38b064"
        }
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Save Binary Tree
### Method: POST
>```
>/tree
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{
    "tree": 
}
```

### Response: 200
```json
true
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get Binary Tree Calculations
### Method: GET
>```
>/tree/
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Response: 200
```json
{
    "sum": 206,
    "path": [
        "b9acba7c-9d21-46cd-a041-d9a9f489c424",
        "02e02109-e7a3-4f18-a3e6-48cf31fd4fac",
        "f0d4e402-94d8-4e7a-acd4-3cd82821bbd2"
    ]
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get User Tree
### Method: GET
>```
>/tree
>```
### Headers

|Content-Type|Value|
|---|---|
|auth-key||


### Response: 200
```json
{
    "tree": {
        "left": {
            "left": {
                "value": 98,
                "uniqueId": "f0d4e402-94d8-4e7a-acd4-3cd82821bbd2"
            },
            "value": 97,
            "uniqueId": "02e02109-e7a3-4f18-a3e6-48cf31fd4fac"
        },
        "right": {
            "right": {
                "value": 73,
                "uniqueId": "ca599dc9-0e74-4a0d-b64d-b00b668df729"
            },
            "value": 13,
            "uniqueId": "dd01c872-9180-4a9d-ab14-1b8948335444"
        },
        "value": 11,
        "uniqueId": "b9acba7c-9d21-46cd-a041-d9a9f489c424"
    },
    "userId": 23,
    "maxSumPath": {
        "maxLeafToNode": {
            "sum": 206,
            "path": [
                "b9acba7c-9d21-46cd-a041-d9a9f489c424",
                "02e02109-e7a3-4f18-a3e6-48cf31fd4fac",
                "f0d4e402-94d8-4e7a-acd4-3cd82821bbd2"
            ]
        }
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
