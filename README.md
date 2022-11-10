# Gritty grammar

# API OVERVIEW
Leverage the Gritty Grammar API to bring seamless language assistance to our users and improve their grammar delivery.
Have a conversation with our AI bot, talk to it like you would with a friend and watch it transcribe as well as spot and correct your grammatical errors.
Perfect when you are learning a new “langwuyage” don’t you think?
Application Programming Interfaces (APIs) are what drives Gritty Grammar API and it is organized around a Representational State Transfer (REST).

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
    "status": "success",
    "_id": "636cc01c23ddfba61a0f41b5",
   "username": "jondoe",
    "email": "js@gmail.com",
    "password": "password",
    "verified": false,
   
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
     "status": "success",
    "username": "jondoe",
    "email": "js@gmail.com",
    "verified": true,
   
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


