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

# frontFinalProgramacionWeb

## Project frontend structure

*Frontend
  *src/
    *components/ 
      *Dashboard.jsx 
    *services/ 
      *metricsService.js 
    *App.jsx
    *main.jsx
  *package.json

The components folder contains the visual components in React of the page 
The services folder contains the connection with the backend, which returns the contents of the main table

## Main components & Handling of States using Hooks

The only 2 components are Dashboard (gets the data from the backend, draws the graph, and is responsible to maintain the state of the page, with useState and acts as the listener with useEffect) and MetricCard (which is called in the Dashboard component and just shows a name and its associated value)

## Consumption of API´s

The only API used in this frontend is a REST GET, used in the services folder to get the information for the graph and metric cards

## Implementation of graphics visulas

For the implementation of the graphs it was used `react-chartjs-2` and `chart.js`. 
`Chart.js` was used to create the data of the graph by mapping the values, then `react-chartjs-2` creates the graph with the data obtained with the previous library

## Fixes
- We could move the second minor component to a new file in the folder, this would keep the code clean
- There is no way for the user to change the type of data the graph should display, it is stuck in commits
