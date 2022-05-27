# Springboot Kafka Testcontainers - Spike

A spike to get familiar with Springboot, Kafka and Testcontainers

Only the Producer is somewhat tested.

## Challenges & Learnings

- It took some time to configuring the bootstrap server dynamically in the test. (Failed to load ApplicationContext..)
- Learning: The testcontainers have to boot up before the spring beans are initialized.
- Testcontainers has DEBUG as the default loglevel, adding a [logback.xml](src/test/resources/logback-test.xml) helped
  to reduce the clutter.
- Learning: springboot already provides a range of configurable kafka variables out of the box. This made a custom
  kafkaTemplate unnecessary.
- podman (WSL) failed to work, because systemctl/systemd is not supported. Switching to Docker Desktop worked.
  Testcontainers only works with docker-api.

# Links

- https://www.testcontainers.org/
- https://spring.io/projects/spring-kafka

This project was bootstrapped with [spring initializr](https://start.spring.io/)
