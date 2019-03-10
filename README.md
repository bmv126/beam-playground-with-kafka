# beam-playground-with-kafka
Reading avro messages from kafka with beam consumer and writing back to Kafka using kafka producer.

A simple Beam Pipeline to show how the data can be read from kafka topic and written back to kafka topic.

Below graph depicts the transformations applied:

  KafkaIORead ---> Pardo (Convert GenericRecord to Row ) ---> Pardo (Convert Row to GenericRecord ) ---> KafkaIoWrite
  
This example is mainly used to show, how records can be converted from one format to another (GenericRecord <--> Row). To keep it simple, same 
avro schema is used at both surce and sink.
