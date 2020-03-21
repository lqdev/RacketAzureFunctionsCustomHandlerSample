# Serverless Racket Application with Azure Functions Custom Handler

This sample application uses Azure Functions Custom Handlers to run a Racket web application as a serverless function.

## Prerequisites

This project was built on a Windows 10 PC, but it should work cross-platform on Mac and Linux.

- [Node.js](https://nodejs.org/en/)
- [Racket](https://download.racket-lang.org/)
- [Azure Functions Core Tools](https://docs.microsoft.com/azure/azure-functions/functions-run-local). This sample uses v2.x of the tool.

## Package the application

```bash
raco exe server.rkt
```

## Run the server (not as an Azure Function)

Enter the following command into the command prompt.

```bash
server.exe
```

Using an application like Postman or Insomnia, make a `GET` request to `localhost:7071/values`.

The response should look the one below:

```json
{
    "value": [
        1,
        2,
        3
    ]
}
```

## Run Azure Function

Enter the following command into the command prompt from the root application directory.

```bash
func start
```

Using an application like Postman or Insomnia, make a `GET` request to `localhost:7071/api/values`.

The response should look the one below:

```json
{
    "value": [
        1,
        2,
        3
    ]
}
```
