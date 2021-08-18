## Real time messaging with websockets

**STOMP** is a subprotocol operating on top of the lower-level WebSocket.<br>


## Using WebSocket to build an interactive web application
1-generate a new project with the required dependency (Websocket).
* implementation 'org.webjars:webjars-locator-core'
* implementation 'org.webjars:sockjs-client:1.0.2'
* implementation 'org.webjars:stomp-websocket:2.3.3'
* implementation 'org.webjars:bootstrap:3.3.7'
* implementation 'org.webjars:jquery:3.1.1-1'
2-model the message that carries the name, create a plain old Java object with a name property and a corresponding getName()
3-model the greeting representation, add another plain old Java object with a content property and a corresponding getContent() method

## Create a Message-handling Controller
1- The `@MessageMapping` annotation ensures that, if a message is sent to the /hello destination, the `greeting<br>()` method is called.<br>
2- After the one-second delay, the `greeting()` method creates a Greeting object and returns it.<br>
The return value is broadcast to all subscribers of /topic/greetings, as specified in the `@SendTo` annotation.

## Configure Spring for STOMP messaging<br>
* Create a Java class named WebSocketConfig<br>

* `@Configuration` to indicate that it is a Spring configuration class.<br>

* `@EnableWebSocketMessageBroker` enables WebSocket message handling, backed by a message broker.<br>

**enableSimpleBroker() to:**

* enable a simple memory-based message broker to carry the greeting messages back to the client on destinations<br> prefixed with /topic<br>
* designates the /app prefix for messages that are bound for methods annotated with `@MessageMapping`<br>
The registerStompEndpoints() method registers the /gs-guide-websocket endpoint,<br>

* enabling SockJS fallback options so that alternate transports can be used if WebSocket is not available.<br>
* The SockJS client will attempt to connect to /gs-guide-websocket and use the best available transport <br>(websocket, xhr-streaming, xhr-polling, and so on).<br>

## Create a Browser Client<br>
This HTML file imports the SockJS and STOMP javascript libraries that will be used to communicate with our<br> server through STOMP over websocket.<br>

