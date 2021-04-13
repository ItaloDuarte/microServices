# microServices
Micro services POC using RabbitMQ / Spring Security / Netflix Eureka Server / Netflix Zuul


# Instructions to execute RabbitMq using Docker

version: '3'
services:
  rabbitmq:
    image: rabbitmq:3.8.3-management
	ports:
	  - 5672:5672
	  - 15672:15672
	volumes:
	  - $PWD/storage/rabbitmq1:/var/lib/rabbitmq
	environment:
	  - RABBITMQ_ERLANG_COOKIE=secret_pass
	  - RABBITMQ_DEFAULT_USER=admin
	  - RABBITMQ_DEFAULT_PASS=admin
volumes:
  rabbitmq:
