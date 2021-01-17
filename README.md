# POS (Point of Sale terminal) data streaming application

This is project is on building a stream application to stream transaction data from several pos terminals to an analytic client. This involves a real time update on the client 

## Technologies
This project was built with Apache Kafka Java and Maven dependency repo.

## Functionality
The stream application consist of a producer API and the Stream API.

The producer API connects to the source of the data, a datastore containing json files. It serializes the files and sends to a input topic (a feed to which records are published). The stream API connects to the input topic to receive the serialized json file, does some aggregation and send to an output topic connected to the client. This is real-time & instantaneous, as the files enter the datastore, it is streamed to the client.

