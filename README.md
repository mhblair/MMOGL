KStreams Test Apps 
======================

| **Test App** | **Description** |
|:----------- |:------------------------------|
| streamtest1 | Content Filter based on XPath |
| streamsest2 | Enrich data from a KTable |

## Build

Given a properly setup go develop environment, just run

```
  go get -d -t .
  go build
```

The resulting binary should be named `sqs-to-kafka` (or `sqs-to-kafka.exe`
on Windows). For further detail, e.g. cross-platform builds and custom build
parameters, please refer to the go-documentation.


## Usage

`sqs-to-kafka` takes the following commandline parameters:

  - `--aws-access-key=STRING`: AWS access key
  - `--aws-secret-key=STRING`: AWS secret key
  - `--aws-region=STRING`: AWS region
  - `--aws-profile=STRING`: AWS profile
  - `--aws-read-config`: read AWS configuration from `~/.aws/config`
  - `--aws-endpoint=STRING`: URL of the AWS endpoint
  - `--sqs-url=STRING`: URL of the SQS queue for incomming messages
  - `--kafka-brokers=STRING`: list of Kafka brokers used for bootstrapping
  - `--kafka-topic=STRING`: Kafka topic for outgoing messages
  - `--metrics-address=HOST:PORT`: Listening address to serve metrics
