![image](images/confluent-logo-300-2.png)

* [Demo list](#demo-list)
* [Running demos](#running-demos)
* [Prerequisities](#prerequisites)


# Demo list

There are multiple demos in this repo that showcase Kafka stream processing on the Confluent Platform.
Some demos run on local Confluent Platform installs (download [Confluent Platform](https://www.confluent.io/download/)) and others run on Docker (install [Docker](https://docs.docker.com/install/) and [Docker Compose](https://docs.docker.com/compose/install/)).

## Where to start

The best demo to start with is [cp-demo](https://github.com/confluentinc/cp-demo), which spins up a Kafka streaming ETL using KSQL for stream processing.
cp-demo also comes with a playbook and video series, and is a great configuration reference for Confluent Platform.


## Full list

| Demo                                       | Local | Docker | Category | Description 
| ------------------------------------------ | ----- | ------ | -------- | ---------------------------------------------------------------------------
| [Avro](clients/README.md)               |   [Y](clients/README.md)   |   N    | Confluent Platform | Examples of client applications using Avro and Confluent Schema Registry
| [CDC with MySQL](https://github.com/confluentinc/demo-scene/blob/master/no-more-silos-mysql/demo_no-more-silos.adoc) | N | [Y](https://github.com/confluentinc/demo-scene/blob/master/no-more-silos-mysql/demo_no-more-silos.adoc) | Data Pipelines | Self-paced steps to setup a change data capture (CDC) pipeline
| [Clickstream](clickstream/README.md)       |   [Y](clickstream/README.md)   |   [Y](https://docs.confluent.io/current/ksql/docs/tutorials/clickstream-docker.html#ksql-clickstream-docker)    | Stream Processing | Automated version of the [KSQL Clickstream demo](https://docs.confluent.io/current/ksql/docs/tutorials/clickstream-docker.html#ksql-clickstream-docker)
| [Cloud clients](clients/cloud/README.md)                 |   [Y](clients/cloud/README.md)   |   N    | Confluent Cloud | Examples of client applications in different programming languages connecting to [Confluent Cloud](https://www.confluent.io/confluent-cloud/)
| [Connect and Kafka Streams](connect-streams-pipeline/README.md) |   [Y](connect-streams-pipeline/README.md)   |   N    | Data Pipeline | Demonstrate various ways, with and without Kafka Connect, to get data into Kafka topics and then loaded for use by the Kafka Streams API
| [CP Demo](wikipedia/README.md)           |   [Y](wikipedia/README.md)   |   [Y](https://github.com/confluentinc/cp-demo)    | Confluent Platform | [Confluent Platform Demo](https://docs.confluent.io/current/tutorials/cp-demo/docs/index.html) with a playbook for Kafka streaming ETL deployments
| [CP Quickstart](pageviews/README.md)           |   [Y](pageviews/README.md)   |   [Y](https://docs.confluent.io/current/quickstart/ce-docker-quickstart.html#ce-docker-quickstart)    | Confluent Platform | [Confluent Platform Quickstart](https://docs.confluent.io/current/quickstart.html)
| [GCP pipeline](https://github.com/confluentinc/demo-scene/blob/master/gcp-pipeline/README.adoc) | N | [Y](https://github.com/confluentinc/demo-scene/blob/master/gcp-pipeline/README.adoc) | Data Pipeline | Work with [Confluent Cloud](https://www.confluent.io/confluent-cloud/) to build cool pipelines into Google Cloud Platform (GCP)
| [Hybrid cloud](ccloud/README.md)                 |   [Y](ccloud/README.md)   |   [Y](ccloud/README.md)    | Confluent Cloud | End-to-end demo of a hybrid Kafka Cluster between [Confluent Cloud](https://www.confluent.io/confluent-cloud/) and on-prem using Confluent Replicator
| [KSQL UDF](https://github.com/confluentinc/demo-scene/blob/master/ksql-udf-advanced-example/README.md) | [Y](https://github.com/confluentinc/demo-scene/blob/master/ksql-udf-advanced-example/README.md) | N | Stream Processing | Advanced KSQL [UDF](https://www.confluent.io/blog/build-udf-udaf-ksql-5-0) use case for connected cars
| [KSQL workshop](ksql-workshop/README.md)   |   [Y](ksql-workshop/README.md)   |   [Y](ksql-workshop/README.md)    | Stream Processing | showcases Kafka stream processing using KSQL and can be run automated or self-guided as a KSQL workshop
| [Microservices ecosystem](microservices-orders/README.md) |   [Y](microservices-orders/README.md)   |   N    | Stream Processing | [Microservices Orders Demo Application](https://github.com/confluentinc/kafka-streams-examples/tree/5.1.0-post/src/main/java/io/confluent/examples/streams/microservices) integrated into the Confluent Platform
| [MQTT](https://github.com/confluentinc/demo-scene/blob/master/mqtt-connect-connector-demo/README.md) | [Y](https://github.com/confluentinc/demo-scene/blob/master/mqtt-connect-connector-demo/README.md) | N | Data Pipeline | Internet of Things (IoT) integration example using Apache Kafka + Kafka Connect + MQTT Connector + Sensor Data
| [Multi datacenter](https://github.com/confluentinc/cp-docker-images/tree/5.1.1-post/examples/multi-datacenter) | N | [Y](https://github.com/confluentinc/cp-docker-images/tree/5.1.1-post/examples/multi-datacenter) | Confluent Platform | This demo deploys an active-active multi-datacenter design, with two instances of Confluent Replicator copying data bidirectionally between the datacenters
| [Music demo](music/README.md)                   |   [Y](music/README.md)   |   [Y](music/README.md)    | Stream Processing | KSQL version of the [Kafka Streams Demo Application](https://docs.confluent.io/current/streams/kafka-streams-examples/docs/index.html)
| [MySQL and Debezium](mysql-debezium/README.md) |   [Y](mysql-debezium/README.md)   |   N    | Data Pipelines | End-to-end streaming ETL with KSQL for stream processing using the [Debezium Connector for MySQL](http://debezium.io/docs/connectors/mysql/)
| [Oracle, KSQL, Elasticsearch](https://github.com/confluentinc/demo-scene/blob/master/oracle-ksql-elasticsearch/oracle-ksql-elasticsearch-docker.adoc) |   N   |   Y    | Data Pipelines | Stream data from Oracle, enrich and filter with KSQL, and then stream into Elasticsearch
| [Postgres, Debezium, KSQL, Elasticsearch](postgres-debezium-ksql-elasticsearch/README.md) |   N   |   [Y](postgres-debezium-ksql-elasticsearch/README.md)    | Data Pipelines | Enrich event stream data with CDC data from Postgres and then stream into Elasticsearch


# Prerequisites

For local installs:

* [Confluent Platform 5.1](https://www.confluent.io/download/)
* Env var `CONFLUENT_HOME=/path/to/confluentplatform`
* Env var `PATH` includes `$CONFLUENT_HOME/bin`
* Each demo has its own set of prerequisites as well, documented in each demo's README

For Docker:

* Docker version 17.06.1-ce
* Docker Compose version 1.14.0 with Docker Compose file format 2.1
