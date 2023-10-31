# gRPC

## What Is It?
gRPC is an open-source remote communication framework developed by Google, based on the RPC (Remote Procedure Call) model and using the HTTP/2 protocol for efficient communications. It allows developers to define services and messages using Protocol Buffers (protobuf) files, providing fast and compact data serialization. gRPC supports multiple programming languages, making it easy to create interoperable clients and servers. It also offers built-in security features, making it an ideal choice for distributed architectures, microservices, and applications requiring secure and high-performance remote communication.

## Protobuf
Protocol Buffers (protobuf) is a binary serialization format developed by Google. Thanks to its compact binary structure, protobuf is more efficient in terms of message size and serialization/deserialization speed than many other data formats, such as JSON or XML.

## Advantages of gRPC
- With Protobuf and HTTP/2, gRPC services offer up to 10 times better performance and API protection than REST+JSON interactions.

- Support for streaming, allowing the execution of multiple operations. gRPC makes this possible through HTTP/2's multiplexing feature, which enables sending or receiving multiple responses or requests simultaneously over a single TCP connection.

## Disadvantages of gRPC
- Limited browser support
As no current web browser can handle HTTP/2 frames, you cannot efficiently call a gRPC service from a browser since gRPC Web relies primarily on HTTP/2. Therefore, you need to use a proxy with gRPC, which comes with several drawbacks.

Sources:

https://appmaster.io/fr/blog/quest-ce-que-le-grpc
