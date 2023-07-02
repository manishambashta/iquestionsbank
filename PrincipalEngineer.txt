##Q1. What are the technology stack that you have worked upon
####Ans1. NodeJS, MongoDB, Angular, Python, PHP, HTML, CSS, Javascript, HAProxy, Lua, Nginx

------------------------------------------------------------------------------------------------------
##Q2. Tell me about the NodeJS Architecture
####Ans2. NodeJS is a Javascript based platform, that is mainly used to create I/O intensive web applications such as chat applications, multi-media streaming sites. It is built upon Google Chrome's V8 Javascript engine.
To manage several concurrent clients, NodeJS employs a "Single threaded event loop design", the Javascript event-based model and Javascript callback mechanism are employed in the NodeJS processing model. It employs
two fundamental concepts:
1 - Asynchronous model
2 - Non-Blocking I/O model

###Components of NodeJS architecture
Requests: Depending upon the action user want to perform, a request can be blocking or non-blocking
NodeJS Server: This accepts the request, processes them and return result to the user
Event Queue: The main use of event queue is to store incoming client requests and send them sequentially to the event loop
Event Loop: Event loop receives request from the event queue and sends out the responses to the client
Thread pool: The thread pool in a NodeJS server are threads of the underlying OS, that NodeJS utilizes to perform blocking operations(like file read, or network operations)
External Resources: In order to handle blocking requests, external resources are used, they can be of any type. (computation or storage)

###Internals of NodeJS architecture

      Javascript Code that we write (100%JS)

              NodeJS              (50%JS and 50%C++)

   V8 engine(30%JS 70%C++)        libUV library(100%C++)


===================================================================================================

      Javascript Code that we write

          Node's JS Side (lib folder in Node repo) 
              - process.binding (connects JS and C++ functions)
              - V8 engine (converts values between JS and C++ world)
          Node's C++ Side (src folder in Node repo)

      libUV library (give Node easy access to underlying OS)

###Event Loop







