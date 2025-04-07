# Email Service

## Overview
This project is a Spring Boot application that provides email sending functionalities. It includes features for sending plain text and HTML emails with attachments. The service listens to Kafka topics for email sending requests.

## Project Structure
- `src/main/java/com/example/emailservicemorningbatch/EmailServiceMorningBatchApplication.java`: Main class to bootstrap the Email Service application.
- `src/main/java/com/example/emailservicemorningbatch/configs/SendEmailConsumer.java`: Kafka consumer class for handling email sending messages.
- `src/main/resources/application.properties`: Configuration file for the Email Service.

## Technologies Used
- Java
- Spring Boot
- Spring Mail
- Spring Kafka
- Maven

## Configuration
The `application.properties` file contains the configuration for the Email Service, including mail server settings and Kafka configurations.

### Example Configuration
```ini
spring.application.name=EmailService
server.port=8082
logging.level.org.springframework=TRACE

# Mail server configurations
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@example.com
spring.mail.password=your_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# Kafka configurations
spring.kafka.bootstrap-servers=localhost:9092
spring.kafka.consumer.group-id=emailService
