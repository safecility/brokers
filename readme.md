## Brokers

For data to pass from IoT devices to servers, gateways and data brokers with varying levels of function act as intermediaries.

For MQTT we can either run our own data broker or use a service - The Things Network for instance offers both a service 
and a deployable instance.

NBIoT needs a SIM of some description and authenticates with a network provider.

These modules take raw data from the devices that have passed down one of these routes and pass them, undecoded, to our pubsub
pipelines. 

Initial authentication should have occurred before reaching these microservices.
Device identification, matching a UID to an internally tracked resource, occurs afterwards:

### MQTT
safecility provides access to existing mqtt brokers (the things network etc) 

the MQTT broker should have performed authentication prior to our microservice accessing the mqtt stream.

### COAP
a simple COAP broker 

our microservice is intentionally lightweight and passes all messages - 
Traffic management depends on how SIM access is controlled and how access to the microservice can be filtered.