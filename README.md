# Config Server


## How to include and run a config server

### Import dependencies

```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-config-server</artifactId>
</dependency>
```

### Enable config server

Add `@EnableConfigServer` annotation to the Spring Boot application.

### Configure config repo

This demo stores config files in itself instead of in a git repository.

```yaml
spring:
  profiles:
    active: native
```

Create a `config` directory under resources, and put all microservices configuration files under this
directory. The configuration file naming convention is `<application-name>.yaml`, e.g. `department-service.yaml`.

## Run application

```bash
mvn spring-boot:run
```

or run the Spring Boot application directly.

## References

- https://docs.spring.io/spring-cloud-config/docs/current/reference/html/#_spring_cloud_config_server