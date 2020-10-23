# Spring Cloud Gateway Circuit Breaker demo

1. Run the demo with `./mvnw spring-boot:run`
2. Navigate to `http://localhost:8080/httpbin/html` - expected response is displayed, CB is not tripped
3. Navigate to `http://localhost:8080/status/500` or `http://localhost:8080/status/404`, this will trigger CB and the failure page will be displayed
4. Check that metrics are registered at `http://localhost:8080/actuator/metrcis`
5. Alternatively, uncomment `wavefront-spring-boot-starter` dependency in `pom.xml` to enable WaveFront integration to visualise CB metrics