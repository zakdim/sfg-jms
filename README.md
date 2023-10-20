# Spring Framework Guru Pet Clinic

[Udemy - Spring Framework 5: Beginner to Guru](https://www.udemy.com/course/spring-framework-5-beginner-to-guru/)

## Section 29: JMS Messaging

### S29-460 Running Active MQ in Docker

[Apache ActiveMQ Artemis](https://hub.docker.com/r/apache/activemq-artemis)

[User Manual](https://activemq.apache.org/components/artemis/documentation/latest/docker.html#official-images)

```
# Run x86 container with Rosetta: --platform linux/amd64
docker run --detach --name mycontainer -p 61616:61616 -p 8161:8161 --rm apache/activemq-artemis:latest-alpine
# With Rosetta:
docker run --platform linux/amd64 --detach --name mycontainer -p 61616:61616 -p 8161:8161 --rm apache/activemq-artemis:latest-alpine

docker exec -it mycontainer /var/lib/artemis-instance/bin/artemis shell --user artemis --password artemis

docker logs -f mycontainer

docker stop mycontainer
```

Once the broker starts you can open the web management console at http://localhost:8161 and log in with the default username & password `artemis`.
