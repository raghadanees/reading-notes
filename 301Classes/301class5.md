## Heroku
View logs
Heroku treats logs as streams of time-ordered events aggregated from the output streams of all your app and Heroku components, providing a single channel for all of the events.

View information about your running app using one of the logging commands, `heroku logs --tail`:

`heroku logs --tail`
`2011-03-10T10:22:30-08:00 heroku[web.1]: State changed from created to starting`
`2011-03-10T10:22:32-08:00 heroku[web.1]: Running process with command:` `node index.js`
`2011-03-10T10:22:33-08:00 heroku[web.1]: Listening on 18320`
`2011-03-10T10:22:34-08:00 heroku[web.1]: State changed from starting to up`
`Visit your application in the browser again, and you’ll see another log message generated.`

#### Press Control+C to stop streaming the logs.



## Node.js
#### Node.js For Beginners. Deploy Your Blog to Heroku
Error pages are not what typically appear on your screen when you're surfing the web, but when it happens it's so annoying! To see how servers work from within, we will build a simple web server by ourselves. We will use Node.js as a server part technology for that task. Then we'll use Heroku cloud application platform to turn this local server into a world wide server.

#### Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform. First of all, of course, you need to install it.  Is it done? Now you can create your first web server. And it will be one of the easiest tasks in your life.

Pretty simple, but it's a server!
First of all, we need to create a JavaScript file. Let's name it server.js:


server.js
var http = require("http");


http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000);

Run at your terminal:

node server.js

Then check it in your browser. Your new server's address, as you may guess, is http://localhost:3000/ .

![Image](https://i.imgur.com/idykoj7.png)


Now, to be sure it's a web server and not just a piece of code that returns a single line of text, we'll use it as a server! You can check it with your smartphone. Let's suppose, your laptop's IP address within your local network is 192.168.1.101. You can connect to your server through the 3000th port (for this particular example) by typing http://192.168.1.101:3000/ in your browser.



But you should notice something, before we go further. Let's look more closely at our first Node server. This is an example of how Node provides you with non-blocking and event-driven behavior. Let me explain:

$.post('/some_requested_resource', function(data) {
  console.log(data);
});
This code performs a request for some resource. When the response comes back, an anonymous function is called. It contains the argument data, which is the data received from that request.

So, Node allows you to use the so-called event loop, which works faster because of non-blocking behavior. For example, nginx uses an event loop with asynchronous I/O. That's why it's fast as hell!

