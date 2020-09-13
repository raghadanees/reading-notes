##  HTTP and REST

*HTTP stands for Hypertext Transfer Protocol. It's a stateless, application-layer protocol for communicating between distributed systems, and is the foundation of the modern web. As a web developer, we all must have a strong understanding of this protocol.*

*HTTP allows for communication between a variety of hosts and clients, and supports a mixture of network configurations.*

*Communication between a host and a client occurs, via a request/response pair. The client initiates an HTTP request message, which is serviced through a HTTP response message in return.*

#### URLs
At the heart of web communications is the request message, which are sent via Uniform Resource Locators (URLs). I'm sure you are already familiar with URLs, but for completeness sake, I'll include it here. URLs have a simple structure that consists of the following components:

![Image](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-url-structure.png)

- The protocol is typically http, but it can also be https for secure communications.


### Verbs

URLs reveal the identity of the particular host with which we want to communicate, but the action that should be performed on the host is specified via HTTP verbs.

GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource.

POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.

PUT: update an existing resource. The payload may contain the updated data for the resource.

DELETE: delete an existing resource.

### Using HTTP in Web Frameworks and Libraries
We'll use ExpressJS for Node, Ruby on Rails, and jQuery Ajax as our examples.



### What is REST
REST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems 

RESTful Endpoint: is a URI (Uniform Resource Identifier) that indentifies the resource that when addressed with a proper method, you can effect state (performing CRUD operations over HTTP).
A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data.

### Term
lifecycle : Application lifecycle is a key way that modern OSs manage resources.

collections : a form of memory management whereby objects that are no longer referenced are automatically deleted and their resources are reclaimed.

the “Repository” design pattern : a kind of container where data access logic is stored.

mongoose middleware : functions that can intercept the process of the init, validate, save, and remove instance methods.

Object Relation Mapping (ORM) : a programming technique for converting data between incompatible type systems using object-oriented programming languages.

 

Resources:
https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177

https://restfulapi.net/

