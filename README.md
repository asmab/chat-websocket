# chat-websocket

Chat room
- Server (Back-end): Spring Boot project with Websocket messaging  
- Client (Front-end): Single web page with Angular 5 
  
  
  ## char-room-server
  
  ### Folder structure 
  
      .
    ├── ...
    ├── src
    │    ├── main
    │       ├── java
    │          ├── chat
    │          │   ├── configuration
    │          │   ├── controllers
    │          │   ├── Application.java
    │          │
    │       ├── resources
    │          ├── application.yml                
    └── ...
    
  pom.xml file contains two dependencies:
  1- spring-boot-starter-web
  2- spring-boot-starter-websocket

  * In the WebSocketConfiguration we override the registerStompEndpoints method to define the endpoint for the clients
  The URL for connection to the server is : [http://localhost:1234/socket/](http://localhost:1234/socket/)
  
  * In the WebSocketController we set up the message Mapping "/send/message" 
  When this URL is triggered , the message will be sent to the clients in /chat subscription
   
