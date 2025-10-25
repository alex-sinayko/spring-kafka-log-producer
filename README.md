# Simple Log Forwarding Service

This is a lightweight service built with **Spring Boot**, designed to forward logs to a **Kafka** topic. It is ideal for
scenarios where you need to reliably send application logs to a robust messaging system for further processing.

## Key Features

- **Log Forwarding to Kafka**: The service pushes logs to Kafka topics, providing a decoupled logging mechanism for
  better scalability and reliability.
- **Dynamic Log Level Configuration**: The configuration includes `management.endpoints.web.exposure.include=*`,
  enabling access to Spring Boot's Actuator endpoints via REST. This allows you to dynamically adjust the logging levels
  without restarting the application.
- **Convenient Log Level Management**: For enhanced usability, the service
  utilizes [Ostara](https://github.com/Trendyol/ostara), a tool designed to simplify log level adjustments within
  distributed applications.

## How It Works

1. Logs are collected and forwarded to a configured Kafka topic.
2. Logging levels can be adjusted in real-time via the `/actuator/loggers` endpoint (exposed by Spring Boot Actuator).
3. Ostara acts as an additional abstraction, enabling simplified log level management through a centralized or
   user-friendly interface.

## Why Use This Service?

This service is built to facilitate seamless integration with modern logging architectures. By leveraging the power of
Kafka for log handling and exposing Spring Boot’s Actuator capabilities for configuration management, it ensures your
application's performance and observability requirements are elegantly met.

For more details about the capabilities of Spring Boot Actuator, refer to
the [official documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/actuator.html).

If you're new to Ostara or interested in simplifying log level management, visit
the [Ostara GitHub repository](https://github.com/Trendyol/ostara) for more information.

---