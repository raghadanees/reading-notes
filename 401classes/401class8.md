## Express Routing & Connected API


- ### *Routing refers to how an application’s endpoints (URIs) respond to client requests.*
- *You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests.*
- *You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function*

- These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

- In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.

###  *Express 4.0 comes with the new Router. Router is like a mini express application. It doesn't bring in views or settings, but provides us with the routing APIs like .use, .get, .param, and route.*
 With the inclusion of the Express 4.0 Router, we are given more flexibility than ever before in defining our routes. To recap, we can:

- Use express.Router() multiple times to define groups of routes
- Apply the express.Router() to a section of our site using app.use()
- Use route middleware to process requests
- Use route middleware to validate parameters using .param()
- Use app.route() as a shortcut to the Router to define multiple requests on a route

### Terms
Middleware : functions that have access to the request object (req), the response object (res), and the next middleware function in the - application’s request-response cycle.

Request Object : what retrieves the values that the client browser passed to the server during an HTTP request.

Response Object : communicates between the server and the output which is sent to the client.

Application Middleware : software that provides services beyond those provided by the operating system to enable the various components of a distributed system to communicate and manage data.

Routing Middleware : determining how an application responds to a client request to a particular endpoint.


#### References
- https://expressjs.com/en/guide/routing.html
- https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4
- https://expressjs.com/en/guide/using-middleware.html