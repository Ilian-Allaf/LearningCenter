# Monolithic Vs Microservice
## Monolithic architecture

let's say you were working on an application that does authentication, processes orders, and, eventually, handles payments. You would bundle all these components, and the application’s database, into a tightly-coupled unit that’s deployed as one application — a monolith.

### limitations of the monolithic architecture

- It’s hard to introduce new changes to a monolith, as well as maintain and upgrade it over time (for example, to update the payment service, you need to test and re-deploye the whole monolith and its replicas)
- Scaling a monolithic application is usually not optimal (for example, to scale the autentication service you need to duplicate the whole monolith)
- Monolithic applications are not resilient — if one part of the system fails, the entire system fails

## Microservice architectuire

Unlike the monolithic architecture, the microservice architecture breaks down an application into smaller, self-reliant components called services.
Each service is developed and deployed separately. As a result, each service runs on a separate process.

## Add a messaging queue to your microservice architecture
A message queue is fundamentally any technology that acts as a buffer of messages — it accepts messages and lines them up in the order they arrive. When these messages need to be processed, they are again taken out in the order they arrive.

In our example, the order processing service is blocked until it receives the response to its request to the payment service

One of the objectives of microservices is to create small independent services that remain operational even if one or more services experience downtime.
However, the fact that the order processing service has to wait idly for a response from the payment service creates a level of interdependence that detracts from the intended autonomy of each service.

That's why implementing an asynchronous communication between order and payment thanks to a messaging queue can be very useful.

Source:

https://www.freecodecamp.org/news/message-queues-in-distributed-systesms/
https://blog.professorbeekums.com/performance-vs-scalability/