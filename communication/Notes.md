# Communication Types

# Synchronous Blocking Communication
- In this of communication, the services blocks the operation & waits for the response

> Implentation
- Request/Response model: Rest over http, RPC

> Advantage
- Simple to use, easy to communicate 

> Disadvantages
- It can result in timeouts in mutliple call execution
- It partially knows the destination application [**Tightly coupled**]

# Asynchronous Non-Blocking Communication
- In this of communication, the services doesnt block the operation & response is sent in future

> Implentation
- Request/Response model: Event driven method - Rest over http [Async way], Topic driven / Queue driven


> Advantage
- It fits well for mutliple call execution
- It doesnt know destination application [**Loosely coupled**]

> Disadvantages
- It is complex in nature
