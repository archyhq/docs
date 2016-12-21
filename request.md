# Request

Archy communicates with Integrations using HTTP protocol. Every time user makes an action in Archy Client, Archy will send a HTTP POST request with JSON payload to the related Integration. Below you can description of such JSON payload.

## HTTP Request Body

```
{
  "payload": {
    "user": {
      "providers": [
        {
          "type": "loginpassword",
          "login": "user login",
          "password": "user password",
          "endpoint": "user endpoint"
        }
      ],
      "id": "b75b36b3-79c8-471b-a51d-4efd60080eb4"
    },
    "nextResultCursor": null,
    "args": {}
  }
  "address": "@developer/namespace/command",
  "action": "execute"
}
```



