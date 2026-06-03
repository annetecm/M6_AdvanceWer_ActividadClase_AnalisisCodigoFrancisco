# backFinalProgramacionWeb

## Project backend structure

- `demo/src/main/java/com/exampleback/demo/config/CorsConfig.java`
  - Configures CORS rules for the API and allows browser requests from other origins.
- `demo/src/main/java/com/exampleback/demo/config/SecurityConfig.java`
  - Sets security rules for HTTP requests and configures basic web security behavior.
- `demo/src/main/java/com/exampleback/demo/controller/MetricsController.java`
  - Exposes REST endpoints to receive metric requests and return metric responses.
- `demo/src/main/java/com/exampleback/demo/dto/MetricRequestDTO.java`
  - Defines the request payload shape for incoming metric queries.
- `demo/src/main/java/com/exampleback/demo/dto/MetricResponseDTO.java`
  - Defines the response payload shape returned by the metrics API.
- `demo/src/main/java/com/exampleback/demo/model/DeveloperMetric.java`
  - Models developer metric data with fields, constructors, getters, and setters.
- `demo/src/main/java/com/exampleback/demo/repository/DeveloperMetricRepository.java`
  - Stores and provides access to hardcoded developer metric records.
- `demo/src/main/java/com/exampleback/demo/repository/MetricResponseDTO.java`
  - Duplicate DTO definition in the repository package (it is not used by the main API flow).
- `demo/src/main/java/com/exampleback/demo/service/MetricsService.java`
  - Contains business logic to process metrics and create API responses.

## Fixes
- There is a duplicated file named `MetricResponseDTO.java` in the `repository` package. It is not used and should be removed to avoid confusion.
- `MetricRequestDTO.java` contains unused code and may need cleanup.
- `MetricResponseDTO.java` in `dto` has simple logic and could be improved with validation or safety checks.
