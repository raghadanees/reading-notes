## API Server

#### router.param(name, callback)
Adds callback triggers to route parameters, where name is the name of the parameter and callback is the callback function. Although name is technically optional, using this method without it is deprecated starting with Express v4.11.0 (see below).

The parameters of the callback function are:

- req, the request object.
- res, the response object.
- next, indicating the next middleware function.
- The value of the name parameter.
- The name of the parameter.

*Unlike app.param(), router.param() does not accept an array of route parameters.*

##### Types of Middleware
Mongoose has 4 types of middleware: document middleware, model middleware, aggregate middleware, and query middleware. Document middleware is supported for the following document functions. In document middleware functions, this refers to the document.

#### Subdocuments
They are documents embedded in other documents. In Mongoose, this means you can nest schemas in other schemas. Mongoose has two distinct notions of subdocuments: arrays of subdocuments and single nested subdocuments.
they are similar to normal documents. Nested schemas can have middleware, custom validation logic, virtuals, and any other feature top-level schemas can use. The major difference is that subdocuments are not saved individually, they are saved whenever their top-level parent document is saved.

### Populate Virtuals

So far you've only populated based on the _id field. However, that's sometimes not the right choice. In particular, arrays that grow without bound are a MongoDB anti-pattern. Using mongoose virtuals, you can define more sophisticated relationships between documents.

## Terms
- Routing:refers to how an application’s endpoints (URIs) respond to client requests.
- Route Prefixing: Route grouping is a concept to make the route function that receive same prefix of different requests.
- Request body: data sent by the client to your API.
- Request “Query” :the values that the client browser passed to the server during an HTTP request
- Request “Params” : is a combination of the keys/values you’ll find in Request.Querystring , Request.Form , Request.Cookies , Request.ServerVariables



Ref
- https://mongoosejs.com/docs/middleware.html
- https://mongoosejs.com/docs/populate.html#populate-virtuals
- https://expressjs.com/en/4x/api.html#router.param
