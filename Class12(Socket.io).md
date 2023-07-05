# Class 12


## [Web Sockets](https://en.wikipedia.org/wiki/WebSocket)



#### 1. What is a Web Socket?

WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.

#### 2. Describe the Web Socket request/response handshake and what happens once the connection is established.

Once the connection is established, communication switches to a bidirectional binary protocol which does not conform to the HTTP protocol.
And the client and server can send WebSocket data or text frames back and forth in full-duplex mode. The data is minimally framed, with a small header followed by payload. WebSocket transmissions are described as "messages", where a single message can optionally be split across several data frames. This can allow for sending of messages where initial data is available but the complete length of the message is unknown


#### 3. Web Sockets provide a standardized way for the server to send content to a client without first receiving a ____ from that client.

requested 



## [Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)



#### 1. What does the event handler io.on() do?

The io.on event handler handles connection, disconnection, etc., events in it, using the socket object.


#### 2. Describe some possible proof of life or proof that the code works as expected



#### 3. What does socket.emit() do?

socket.emit function can create and fire custom events.




## [Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)



#### 1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).

WebSocket is a communication protocol that facilitates bidirectional communication between a client and a server over a TCP connection. It differs from traditional HTTP communication by keeping the connection open continuously, allowing for real-time data transfer. When a client sends a request to the server, the connection is not closed upon receiving the response. Instead, it remains open, persisting until either the client or server terminates the request.

Socket.IO, on the other hand, is a library that enables real-time and full-duplex communication between clients and web servers. It utilizes the WebSocket protocol as its underlying interface. Socket.IO is typically divided into two parts and serves as an event-driven library.


#### 2. When would you use Socket.IO?

-It handle all the degradation of your technical alternatives to get full-duplex communication in real-time.

-It also handles the various support level and the inconsistencies from the browser.

-It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.

-Currently, AFAIK is the most used one and easier to help with vanilla web sockets.


#### 3. When would you use WebSockets?

-It provides full-duplex communication, which helps in persisting the connection established between the Client and the Web Server.

-It also lives up to the standards and provides the accuracy and efficiency stream events to and from with negligible latency.

-WebSocket removes the overhead and reduce complexity.

-It makes real-time communication effortless and efficient.

### Videos:

## [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)



#### 1. What are a couple of key takeaways from this video?

-OSI model is the system that manage the network between the devices.

-OSI model consists of 7 layers: application, presentation, session, transport, network, datalink, physical.

-each layer have his own protocols to work in a specific part of the network


## [TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)



#### 1. Translate the gist of this video to a non-technical friend

In simple terms, it means that the client requests the server to establish a connection with it. The server responds by accepting the connection and asking the client to open the communication line. The client acknowledges the request, and thus the connection is formed.



### Bookmark and Review

## [Socket.io Documentation](https://socket.io/docs/)

## [Socket.io Server API](https://socket.io/docs/server-api)

## [Socket.io Client API](https://socket.io/docs/client-api)

## [Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)




