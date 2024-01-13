HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack (TCP/IP).

it is stateless; there is no link between two requests being successively carried out on the same connection. while the core of HTTP is stateless, HTTP cookies allow use of stateful sessions. using header extensibility, HTTP cookies are added to the workflow.

# HTTP messages
there are 2 types of HTTP messages, requests and responses.

## Requests

```http
GET /home HTTP/1.1
Host: localhost:8000
Accept-Language: en-US
```

requests consist of the following elements:
- an HTTP method, usually a verb like `GET`, `POST` that defines the operation the client wants to perform
- the path of the resource to fetch; the URL of the resource stripped from elements that are obvious from the context
- the version of the protocol
- optional headers that convey additional information to the servers
- a body for methods like `POST` and `PATCH`

## Responses

```http
HTTP/1.1 200 OK
Server: Apache
Content-Type: application/json
```

responses consists of the following elements:
- the version of the HTTP protocol they follow
- a `status code`, indicating if the request was successful or not
- a `status message`, a non-authoritative short description of the status code
- HTTP headers, like those for requests
- optionally, a body containing the fetched resource

# resources
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview
- 