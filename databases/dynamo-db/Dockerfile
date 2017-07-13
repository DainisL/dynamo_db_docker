FROM openjdk:8-jre
MAINTAINER Dainis Lapins <dainis186@gmail.com>

WORKDIR /var/dynamodb

RUN wget -O /tmp/dynamodb_local_latest https://s3-us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.tar.gz && \
    tar xfz /tmp/dynamodb_local_latest && \
    rm -f /tmp/dynamodb_local_latest

ENTRYPOINT ["/usr/bin/java", "-Djava.library.path=.", "-jar", "DynamoDBLocal.jar", "-dbPath", "/var/dynamodb_local_vm"]
CMD ["-port", "8000"]

VOLUME ["/var/dynamodb_local_vm", "/var/dynamodb/db"]
