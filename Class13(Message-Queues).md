# Class 13


## Message Queues

### [Socket.io Chat Example](https://socket.io/get-started/chat/)



#### 1. Explain to a non-technical recruiter what the Chat Example (above) does.

it allows the users to connect with the server and communicate in real time.


#### 2. What proof of life are we getting on the backend from the above app?

once the other users are connected we get a message on the console or seeing the stauts of the user saying "a user connected".



#### 3. Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?

io.broadcast.emit()


## [Rooms](https://socket.io/docs/v4/rooms)



#### 1. What is a room and how might a room be useful?

A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

#### 2. How do you join a room?

You can call join to subscribe the socket to a given channel:

io.on("connection", (socket) => { socket.join("some room"); });

And then simply use to or in (they are the same) when broadcasting or emitting:


#### 3. how do you leave a room?

Upon disconnection, sockets leave all the channels they were part of automatically, and no special teardown is needed on your part.

You can fetch the rooms the Socket was in by listening to the disconnecting event.



## [Namespaces](https://socket.io/docs/v4/namespaces/)



#### 1. What is a Namespace and what does it allow you to do?

A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called "multiplexing").

#### 2. Each namespace potentially has its own what? (hint: 3 things)

-event handlers

-rooms

-middlewares


#### 3. Discuss a possible use case for separate namespaces

you want to create a special namespace that only authorized users have access to, so the logic related to those users is separated from the rest of the application.

your application has multiple tenants so you want to dynamically create one namespace per tenant.





### Bookmark and Review:

## [Socket.io Emit Cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)

