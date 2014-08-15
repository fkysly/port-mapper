port-mapper
===========

A port mapping tool by node.js which helps accessing a back server (in LAN, etc), via a front server having public ip(s) and a client server that could access the back server.
Tested on Minecraft 1.7.2 server.

The project is published under GPLv2 License.

[Principle introduce (Simplified Chinese)][1]

###Other languages
* [简体中文][2]

##Requirements

 * A front server has public ip(s)
 * A client server that can access the back server (You can just use the back server)
 * node.js runtime on **both** front and client server

##How to
 1. Edit settings in *server.js* and *client.js* .
 2. Upload files to both servers.
 3. Run *server.js* on the **front** server.
 4. Run *client.js* on the **client** server.

***[Notice] You must do the step 3 first, or the client won't work correctly.***

##Config Definition
*[Notice] You must keep settings in server.js the same as those in client.js.*

### server.js
```javascript
var PUBLIC_PORT   = 80; // The port you can access from internet
var CONNECT_SIGN  = ''; // Auth been the two server and avoid unexpected forward
var CONNECT_PORT  = 1201; // The port to connect with the front server
var TRANS_PORT    = 1202; // The port to trans to the front server
```
### client.js
```javascript
var GATEWAY       = ''; // The ip or domain of the front server

var SERVER_HOST   = ''; // The ip or domain of the back server
var SERVER_PORT   = 80; // The port of service on the back server 

var CONNECT_SIGN  = ''; // Auth been the two server and avoid unexpected forward
var CONNECT_PORT  = 1201; // The port to connect with the front server
var TRANS_PORT    = 1202; // The port to trans to the front server
```

  [1]: PRINCIPLE.md
  [2]: README.zh_CN.md
