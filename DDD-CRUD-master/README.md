

# Back-end

For the Web API infrastructure I used .NET 6, implementing the Domain-driven design pattern using "clean" architecture.
The API is divided into 3 different layers:
- Application layer (WebAPI folder)
- Domain layer
- Infrastructure layer

Overview of the interaction between layers:
![Architecture helper image](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/media/ddd-oriented-microservice/ddd-service-layer-dependencies.png)

Relevant details:
- Used **LiteDB** as the database for this project due to its ease of use and very low overhead, which I implemented utilizing the **repository pattern**.
- Implemented the IReportService, which controls the repositories and the validation of the ReportAggregate Entities.
- Used FluentValidation for validation, located inside the infrastructure layer.

# Front-end

The frontend is rather crude since I did not have much experience with browser-based frameworks like Angular.
It consists of:
- A Material-based design with Material widgets (kudos to Google).
- A main table that lists all ReportAggregates and their properties.
- The ability to create, update, and delete ReportAggregates and their respective ReportItems.



