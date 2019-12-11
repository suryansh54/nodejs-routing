# Node JS Routing
Routing defines the way in which the client requests are handled by the application endpoints.

Implementation of routing in Node.js: There are two ways to implement routing in node.js which are listed below:
- Without using Framework
- By Using Framework

### Node JS Routing without using Framework
```javascript
var http = require('http');
//create a server object:
http.createServer(function (req, res) {
 res.writeHead(200, {'Content-Type': 'text/html'}); // http header
var url = req.url;
 if(url ==='/about'){
    res.write('<h1>about us page<h1>'); //write a response
    res.end(); //end the response
 }else if(url ==='/contact'){
    res.write('<h1>contact us page<h1>'); //write a response
    res.end(); //end the response
 }else{
    res.write('<h1>Hello World!<h1>'); //write a response
    res.end(); //end the response
 }
}).listen(3000, function(){
 console.log("server start at port 3000"); //the server object listens on port 3000
});
```
- http://localhost:3000
- http://localhost:3000/about
- http://localhost:3000/contact

### Routing with express

For GET request use app.get() method
```javascript
var express = require('express')
var app = express()

app.get('/', function(req, res) {
    res.send('Hello Sir')
})

app.listen(3000, function(){
 console.log("server start at port 3000"); //the server object listens on port 3000
});
```

For POST request use app.post() method:
```javascript
var express = require('express')
var app = express()

app.post('/', function(req, res) {
    res.send('Hello Sir')
})

app.listen(3000, function(){
 console.log("server start at port 3000"); //the server object listens on port 3000
});
```
