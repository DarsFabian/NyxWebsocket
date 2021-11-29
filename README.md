# Nyx Websocket

Nyx Websocket is a personnal C implementation of the Websocket technology as specified by [RFC6455](https://datatracker.ietf.org/doc/html/rfc6455). It should be designed to be lightweight and as easy to use as possible, in contrast with most C/C++ implementations.

![](https://carbon.now.sh/?bg=rgba%28125%2C197%2C220%2C1%29&t=one-dark&wt=none&l=auto&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=69px&ln=false&fl=1&fm=Fira+Code&fs=14px&lh=144%25&si=false&es=2x&wm=false&code=%2523include%2520%253Cnyx%252Fwebsocket%253E%250A%250Avoid%2520handleData%28Data%2520data%29%2520%257B%250A%2509Do%2520stuff...%250A%257D%250A%250Aint%2520main%28%29%2520%257B%250A%2509websocket%2520nyx%2520%253D%2520createWebsocket%28%29%253B%250A%2509nyx.on%28%27data%27%252C%2520handleData%29%253B%250A%2520%2520%2520%2520%250A%2520%2520%2520%2520return%25201%253B%250A%257D%250A)

## Summary

 1. [Documentation and installation](##-Documentation-&-Installation)
 2. [Issues, questions, features](##-Ran-into-a-problem?-Any-questions?-Missing-any-feature?)
 3. [Performance](##-Performance)
 4. [Notes](##-Notes)
 5. [Todo](##-Todo)
 6. [Contacts](##-Contacts)

## Documentation & Installation
Nyx Websocket doesn't have any documentation at the moment. Besides, it doesn't even provide any library for now. I will be adding a documentation as soon I feel like the project might need one.

## Ran into a problem? Any questions? Missing any feature?
No problem! You're welcome to open an issue and describe the steps I must follow to reproduce it. Likewise, if you have any question or requests open an issue or feel free to contact me on any socials listed in the [contacts](##Contacts) section.


## Performance

It is designed and thought in a manner to be as lightweight as possible, therefore, feel free to contribute, I am still learning and I would appreciate to learn best/good practices.

## Notes

**This project is not finished and should never be used in production.** As stated above, it may be unhealthy performance-wise, and **might break very frequently.** As for now at least.

## Todo

This section is an incomplete list of what needs to be done. It should be complete at the end of the project.

| Status | Description |
|--|--|
| Unfinished | If the already has a Websocket connection to the remote host, the client must wait until the connection has been established or must wait for that connection to fail. The client should have only one connection in a `CONNECTING` state. The client must serialize its connections if there are more than one at a time. |
| Unfinished | If secure is true, the client MUST perform a `TLS handshake` over the connection after opening the connection and before sending the handshake data. If it can't it should abort the connection. |
| Unfinished | If the client connected, the client must send an opening handshake to the server. It should be a valid HTTP request, its method should be GET, the header should have a HOST field which contains `/host/` and the port if the default is not used. It should have an UPGRADE header field which must include the keyword "websocket". |
| Unfinished | The header should have a `Sec-WebSocket-Key` field containing a randomly selected 16-byte value encoded in base 64 |
| Unfinished | The request MUST include a header field with the name `Origin`. It contains the value of the ASCII serialization of origin of the context in which the code establishing the connection is running. See [RFC6454](https://datatracker.ietf.org/doc/html/rfc6454), [RFC6454](https://datatracker.ietf.org/doc/html/rfc6454) |
| Unfinished | If attempting to establish a connection to `ww2.example.com`, the value of the the header field should be `http://www.example.com`. |
| Unfinished | The request MUST include a header field with the name `Sec-WebSocket-Version`.  The value of this header field MUST be 13. |
| Unfinished | The request MAY include a header field with the name `Sec-WebSocket-Protocol`. If present, this value indicates one or more comma-separated subprotocol the client wishes to speak ordered by preference. The elements that comprise this value MUST be non-empty strings with characters in the range U+0021 to U+007E not including separator characters as defined in [RFC2616](https://datatracker.ietf.org/doc/html/rfc2616) and MUST all be unique strings. |
| Unfinished | The request MAY include a header field with the name `Sec-WebSocket-Extensions`. If present this value indicates the protocol-level extension(s) the client wishes to speak. |
 And so on... More specifications listed in [RFC6455](https://datatracker.ietf.org/doc/html/rfc6455)'s fourth section will be added in the future as the project goes on.


## Contacts
 Will be added later.