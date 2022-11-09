# HNGi9 Grammerly

# API Reference
- Base URL: https://

## Endpoints

`POST /signup`

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

`POST /signin`

- Request body (JSON):

```json
{
    "username": "jondoe",
    "password": "qwerty",
}
```
- Response:

`GET /question`

Randomly gets a question from a bank of questions to ask the user.
- Request body (JSON): None

- Response:

Success

```json
{
    "status": "success",
    "id": "questionId",
    "question": "AI bot's question to the user.",
}
```

`POST /answer`

Sends back a request with the audio answer to the question.
- Request body (JSON):

```json
{
    "id": "questionId",
    "answer": "<answer.mp3>"
}
```

- Response:

Success

```json
{
    "status": "success",
    "errorFreeText": "Error free Transcribed audio",
    "errorFreeAudio": "Error free audio"
}
```