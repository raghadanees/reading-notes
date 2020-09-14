#  Express

### ExpressJS - Middleware
- *Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers, etc.*

#### Order of Middleware Calls
 - One of the most important things about middleware in Express is the order in which they are written/included in your file; the order in which they are executed, given that the route matches also needs to be considered.

 - The following diagram summarizes what we have learnt about middleware 

 ![Image](https://www.tutorialspoint.com/expressjs/images/middleware_desc.jpg)

### Routing
 - Routing refers to how an application’s endpoints (URIs) respond to client requests.
 - You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function 
 These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.

## Terms
SOAP : Simple Object Access Protocol.

ReST Verbs : POST, GET, PUT, PATCH, and DELETE

CRUD Verbs : create, read, update, and delete

Swagger : a set of rules (in other words, a specification) for a format describing REST APIs, that help us document our APIs.




 REF
 - https://expressjs.com/en/guide/routing.html
 - https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm
 - https://expressjs.com/en/guide/using-middleware.html
 - https://www.youtube.com/watch?v=9HOem0amlyg

 