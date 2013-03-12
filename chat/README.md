# Chat Sample

This is a chat sample, which demonstrates the use of Pedestal with...

- Server-Sent Events (SSE)
- Cookies
- Routing
- Interceptors

Prerequisite: all Pedestal libraries, both server and client, must be installed.

To run from the `chat` directory...

```
cd chat-client
lein repl
(dev)
(watch :development)
```
Open another terminal, then:

```
cd chat-server

mkdir resources
cd resources

ln -s ../../chat-client/out/public
cd ..

lein repl
(require 'dev)
(dev/start)  # Launch webserver on port 8080.
```

In a browser, navigate to http://localhost:8080/chat-client-dev.html where you will see the chat client interface.

Use the interface to send a chat message, which you will see echoed to your local screen.

If you play with a friend, you will both see each other's messages.