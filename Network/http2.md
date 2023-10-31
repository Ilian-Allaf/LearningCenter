# HTTP2 main features

## Server push

It allows the server to actively pushes additional resources to the client without the client needing to explicitly request them. This feature is particularly useful for improving website performance because it allows the server to anticipate the resources the client will need and send them before the client requests them.

## Improved Compression

The headers and body of HTTP2 messages are compressed in binary, reducing the load on the network compare to HTTP1 which uses text.

## Multiplexing

HTTP/2 supports multiplexing, which means that multiple requests and responses can be sent simultaneously over the same connection, which improve the loading speed of web pages.

## Prioritization

It allows for the prioritization of requests, meaning that browsers and servers can determine the order in which resources are loaded, thus enhancing the user experience.