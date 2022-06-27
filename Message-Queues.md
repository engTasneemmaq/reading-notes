## Message Queues 👋 👩🏻‍💻

## Socket.io Chat Example: 👀 📝
In this example, a basic chat application is created where there is a bi-directional communication channel between a client and a server.

Broadcasting is for us to emit the event from the server to the rest of the users. io.emit('someEvent',payload).

To send a message to everyone except for a certain emitting socket, we have the broadcast flag for emitting from that socket:



***io.on('connection', (socket) => {
  socket.broadcast.emit('hi');
});***

![chat app](./assest/chat.png)


## Rooms >> 👀 📝
A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

![room](./assest/room.png)


##  To join a room: join() <br>
**io.on("connection", (socket) => {
  socket.join("some room");
});**


## Emitting/Broadcasting: to/in
1. **io.to("some room").emit("some event");**


2. **io.on("connection", (socket) => {
  socket.to("some room").emit("some event");
});**


## To leave a room: leave() just like join().
Private messages: based on SocketID

**io.on("connection", (socket) => {
  socket.on("private message", (anotherSocketId, msg) => {
    socket.to(anotherSocketId).emit("private message", socket.id, msg);
  });
});**




## Namespaces >> 👀 📝
A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called “multiplexing”).

![namespace](./assest/namspace.png)

![namespace](./assest/namespace1.png)


## Each namespace has its own:
- Event handlers.
- Rooms.
- Middlewares.


## Main namespace is: /
io.emit("hello"); is actually equivalent to io.of("/").emit("hello");. io.sockets is an alias for io.of("/").


## Multiplexing will be disabled in the following cases:
- Multiple creation for the same namespace.
**const socket1 = io();
const socket2 = io(); // no multiplexing, two distinct WebSocket connections**


- Different domains.
**const socket1 = io("https://first.example.com");
const socket2 = io("https://second.example.com"); // no multiplexing, two distinct WebSocket connections**

- Usage of the forceNew option
**const socket1 = io();
const socket2 = io("/admin", { forceNew: true }); // no multiplexing, two distinct WebSocket connections**



## Dynamic namespaces
**io.of(/^\/dynamic-\d+$/);**




## References:
1. [Socket.io Chat Example](https://socket.io/get-started/chat/)

2. [Rooms](https://socket.io/docs/v4/rooms)

3. [namespace](https://socket.io/docs/v4/namespaces/)




[Back to the main page  ✔️](README.md)