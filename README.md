# Project Name

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

`POST /api/signin`

- Request body (JSON):

```json
{
    "username": "jondoe",
    "password": "qwerty",
}
```
- Response:

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


