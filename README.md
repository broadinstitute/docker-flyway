# Docker Flyway

Dockerized Flyway command line tool: https://flywaydb.org/documentation/
Built off Flyway version 4.0.3

## To Build

```shell
docker build -t broadinstitute/docker-flyway .
```

## To Run

Mount source code as a volume.
Keystore and truststore can be passed through as `JAVA_ARGS`
```shell
docker run --rm -v $(pwd):/flyway/sql -e JAVA_ARGS=$JAVA_ARGS broadinstitute/docker-flyway [flyway cli args here]
```

