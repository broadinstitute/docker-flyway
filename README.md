# Docker Flyway

Dockerized Flyway command line tool: https://flywaydb.org/documentation/.  Built off Flyway version 4.0.3

Automated build to the broadinstitute/docker-flyway dockerhub repo: 

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

To add a wait before executing, include var `SLEEP` set as num of seconds to sleep before start up.
