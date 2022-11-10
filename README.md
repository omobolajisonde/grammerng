# Gritty grammar

# API OVERVIEW
Project name, is a grammar checking and correction tool that check users grammar and make necessary correction.
APIs Application Programming Interfaces or APIs are what drives (project name here) and it's organized around REST.

# API Reference
- Base URL: https://

## Endpoints

`POST /api/signup`

- Request body (JSON):

```json
{
    "username": "jondoe",
    "email": "js@gmail.com",
    "password": "qwerty",
    "confirmPassword": "qwerty"
}
```
- Response:
SUCCESS

```json
{
   "username": "jondoe",
    "email": "js@gmail.com",
    "password": "$2a$10$hjY6qClu02ghKlof4Ae1CeOjSb96jGX3rx.nKK7SfKVtW3gG05g.a",
    "verified": false,
    "_id": "636cc01c23ddfba61a0f41b5",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYzNmNjMDFjMjNkZGZiYTYxYTBmNDFiNSIsImVtYWlsIjoiYWthbmJpb2xhd2FsZTIwMjJAZ21haWwuY29tIiwiaWF0IjoxNjY4MDcxNDUyfQ.A4oHvVupcZb5iVghy9Qr5vdDu0bN6Kds-bLUcAR3fbs",
    "createdAt": "2022-11-10T09:10:52.865Z",
    "updatedAt": "2022-11-10T09:10:52.865Z",
}

```


ERROR

```json
{
    "status": "error",
    
    "msg": "email already exists"

    
}
```

`POST /api/signin`

- Request body (JSON):

```json
{
    "username": "jondoe",
    "password": "qwerty",
}
```
- Response:
SUCCESS

```json
{   
    "username": "jondoe",
    "password": "qwerty",
    "email": "js@gmail.com",
    "password": "$2a$10$lZ8gnk/nC3m6dFHj4a86eeHBiwG3b/82HpjLaaMtACECAh3XnsIxq",
    "verified": true,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYzMTI0NGY2YWVhZGE1ZTMyM2M2OTQ5YSIsImVtYWlsIjoid2FsZXR0OTVAZ21haWwuY29tIiwiaWF0IjoxNjY4MDcxNzk0fQ.y0RCIrFdN5IUq7K2mAIaEPtVlTgOzvFVU1R5CZ6qoK8",
    "createdAt": "2022-09-02T18:01:26.376Z",
    "updatedAt": "2022-09-06T12:31:08.526Z",
}

```


ERROR

```json
{
    "status": "error",
    
   "msg": "Invalid Credentials"

    
}
```

`post /api/conversation`

starts conversation with our api.

Reuest body:

```json
{
    "conversation_in_Text_Format": "Conversation.txt",

}

OR

{

    "conversation_In_Audio_Format": "<conversation.mp3>",
}

```
Sends back a response with both text and  audio.

- Response:

SUCCESS

```json
{
    "status": "success",
    "id": "conversationId",
    "errorFreeText": "Error free Transcribed audio",
    "errorFreeAudio": "Error free audio",
    "rsponse": "AI bot's success response both audio and text_format.",
}

```


ERROR

```json
{
    "status": "erro",
    "id": "conversationId",
    "errorFreeText": "Error Transcribed audio",
    "errorFreeAudio": "Error audio",
    "rsponse": "AI bot's error response both audio and text_format.",
    
}
```


