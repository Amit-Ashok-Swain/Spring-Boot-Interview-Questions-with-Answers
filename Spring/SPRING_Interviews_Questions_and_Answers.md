## Basics Interviews Questions Of Spring and SpringBoot

1. **What is Spring Framework and its core features?**
    - Spring is a comprehensive framework for building enterprise applications in Java.
    - Core features include dependency injection (IoC), Aspect-Oriented Programming (AOP), Spring MVC, data access, and more.


2. **What are the benefits of using Spring Framework?**
    - Simplifies application development.
    - Promotes loose coupling and easy unit testing.
    - Provides support for AOP, transaction management, and data access.


3. **What is inversion of control (IoC) and dependency injection (DI) in Spring?**
    - IoC is a design principle where control of object creation and lifecycle is shifted to a container.
    - DI is a pattern where objects receive their dependencies from an external source (container).


4. **How does Spring implement DI and what are the different types of DI?**
    - Spring implements DI through constructor injection and setter injection.
    - Constructor injection passes dependencies through the constructor, while setter injection uses setter methods.


5. **What is the Spring Bean lifecycle?**
    - The Spring Bean lifecycle consists of initialization (calling `init` methods) and destruction (calling `destroy` methods).


6. **What is the difference between singleton and prototype scope in Spring?**
    - Singleton creates a single instance of a bean for the entire application.
    - Prototype creates a new instance of the bean whenever requested.

| Aspect                   | Singleton Scope        | Prototype Scope        |
|--------------------------|------------------------|------------------------|
| Object Creation          | Singleton scope creates a single shared instance per Spring container. | Prototype scope creates a new instance every time a bean is requested. |
| Usage                    | Suitable for stateless beans or beans that should be shared globally. | Suitable for stateful beans or those where a new instance is needed on every request. |
| State Management        | Singleton beans maintain state across multiple requests. | Prototype beans typically have a shorter lifespan and don't maintain state. |
| Dependency Injection    | Singleton beans can be injected into other beans. | Prototype beans can also be injected but may lead to a new instance every time. |
| Thread Safety            | Singleton beans should be thread-safe, as they are shared among multiple clients. | Prototype beans are generally not shared across threads and may have less strict thread-safety requirements. |


7. **How do you configure a Spring application using XML configuration?**
    - Create an XML configuration file.
    - Define beans and their dependencies in the file.
    - Use the Spring container to load and manage beans.


8. **What is Spring MVC and how does it work?**
    - Spring MVC is a framework for building web applications.
    - It works by mapping incoming HTTP requests to controller methods and rendering views as responses.


9. **What are the different components of Spring MVC architecture?**
    - Model (business logic), View (UI), and Controller (request handling).


10. **How do you handle exceptions in Spring MVC?**
    - Use exception handling mechanisms like `@ExceptionHandler` or global exception handlers.
    - Define error pages in the web.xml file.

    
11. **What is Spring Security and how does it work?**
    - Spring Security is a framework for securing Java applications.
    - It works by providing authentication, authorization, and various security features for application protection.


12. **How do you configure Spring Security in a Spring Boot application?**
    - Add Spring Security as a dependency.
    - Configure security settings using Java configuration or annotations.


13. **What is Spring Data JPA and how does it work?**
    - Spring Data JPA simplifies data access with JPA (Java Persistence API).
    - It provides repository interfaces that allow querying databases using method names.


14. **What is the difference between Hibernate and Spring Data JPA?**
    - Hibernate is an Object-Relational Mapping (ORM) framework.
    - Spring Data JPA builds on JPA and provides higher-level abstractions for data access.

| Aspect                     | Hibernate                                  | Spring Data JPA                           |
|----------------------------|--------------------------------------------|------------------------------------------|
| Framework Purpose         | Object-Relational Mapping (ORM) framework for mapping Java objects to database tables. | Part of the Spring ecosystem, it simplifies data access and integrates with JPA. |
| Configuration             | Requires configuration files (XML or annotations) for mapping and settings. | Uses JPA annotations and relies on the Spring context for configuration. |
| API                         | Provides a comprehensive ORM API for data access and manipulation. | Offers a simplified and standardized JPA API. |
| Integration                | Can be used with or without Spring. Often integrated with Spring for better control. | An integral part of the Spring framework, providing JPA support. |
| Data Access                | Provides low-level SQL queries and advanced ORM features. | Offers high-level data access with less focus on SQL. |
| Flexibility                | Offers more control and fine-grained customization of queries and caching. | Focuses on reducing boilerplate code and simplifying data access. |
| Maintenance              | Requires more effort for configuration and maintenance. | Simplifies data access and maintenance tasks. |
| Learning Curve          | May have a steeper learning curve due to its extensive features. | Easier for developers already familiar with JPA. |
| Community                | Has a large and established community. | Benefits from the broader Spring community. |


15. **What is AOP in Spring and how does it work?**
    - AOP (Aspect-Oriented Programming) allows modularizing cross-cutting concerns.
    - Spring AOP uses aspects, advice, and pointcuts to intercept and modify method behavior.


16. **What is Spring Boot, and how does it work?**
    - Spring Boot is a project that simplifies Spring application development.
    - It uses convention over configuration to create standalone, production-ready Spring-based applications.


17. **What is the difference between Spring and Spring Boot?**
    - Spring is a comprehensive application framework.
    - Spring Boot is an extension of Spring that simplifies application setup and development.

| Aspect                   | Spring                                      | Spring Boot                                   |
|--------------------------|--------------------------------------------|----------------------------------------------|
| Framework Purpose       | A comprehensive application framework that provides various modules for building enterprise applications. | A project within the Spring ecosystem that simplifies and accelerates the development of stand-alone Spring applications. |
| Configuration             | Typically requires extensive configuration, often through XML or Java-based configuration classes. | Promotes convention over configuration, reducing the need for extensive configuration. Uses sensible defaults for rapid development. |
| Boilerplate Code       | Developers often need to write a significant amount of boilerplate code for setting up various components and configurations. | Reduces boilerplate code through auto-configuration, allowing developers to focus more on application logic. |
| Embedded Servers     | Does not provide built-in support for embedded servers. Deployment often requires external web servers, such as Tomcat or Jetty. | Includes support for embedded servers like Tomcat, Jetty, and Undertow, simplifying deployment and testing. |
| Microservices            | Suitable for building microservices but may require additional configuration for each microservice. | Especially well-suited for developing microservices with minimal configuration, making it a popular choice for microservices architecture. |
| Learning Curve        | May have a steeper learning curve due to its extensive features and configuration options. | Easier for developers to get started with, making it more approachable, especially for beginners. |
| Project Structure     | Developers need to define project structures and dependencies explicitly. | Promotes a predefined project structure, and dependencies are automatically managed using "starters." |
| Customization           | Provides extensive customization and flexibility for various components. | Encourages convention-based configuration but allows customization when needed. |
| Community              | Benefits from a large and active community. | Gaining popularity, with a growing community and support. |
| Use Cases               | Suitable for both small and large applications, with flexibility for customization. | Ideal for building microservices and stand-alone applications quickly, making it well-suited for modern development. |


18. **What is the purpose of Spring Boot and how does it simplify Spring development?**
    - Spring Boot simplifies setup, configuration, and deployment of Spring applications.
    - It provides embedded servers and auto-configuration to reduce boilerplate code.


19. **How do you create a RESTful web service using Spring Boot?**
    - Define a Controller with REST endpoints.
    - Use annotations like `@RestController` and `@RequestMapping` to expose APIs.


20. **What are the advantages of using Spring Boot?**
    - Simplified setup and configuration.
    - Built-in templates, security, and embedded servers.
    - Auto-configuration and production-ready features.


21. **What is Spring Cloud, and how does it simplify microservices development?**
    - Spring Cloud is a framework for building microservices-based applications.
    - It simplifies development by providing tools for service discovery, configuration management, and more.


22. **What are the different types of testing frameworks in Spring, and how do you use them?**
    - Spring supports testing with JUnit, TestNG, and Spring Test.
    - You use these frameworks to write and execute unit, integration, and end-to-end tests.


23. **What are the different features provided by Spring Boot?**
    - Spring Boot offers features like auto-configuration, embedded servers, and externalized configuration.
    - It simplifies security, data access, and more.


24. **What are the steps to create a Spring Boot project?**
    - Use Spring Initializer or start.spring.io to generate a project.
    - Choose project settings, dependencies, and download the code.


25. **What is Spring Boot Auto-configuration?**
    - Spring Boot Auto-configuration automatically configures application components.
    - It simplifies setup by providing sensible defaults based on the project's dependencies.


26. **What is Spring Boot Starter?**
    - A Spring Boot Starter is a pre-configured set of dependencies.
    - It simplifies dependency management and reduces boilerplate configuration.


27. **What is the purpose of the Spring Boot Starter project?**
    - Spring Boot Starters provide a convenient way to set up specific types of projects.
    - They bundle related dependencies for common use cases.


28. **What is the difference between a Spring Boot project and a Spring project?**
    - A Spring Boot project is a stand-alone application with built-in features.
    - A Spring project requires more manual configuration and setup.


| Aspect                   | Spring Project                            | Spring Boot Project                         |
|--------------------------|--------------------------------------------|----------------------------------------------|
| Configuration           | Requires extensive configuration for various components using XML or Java-based configuration classes. | Promotes convention over configuration, reducing the need for extensive configuration. Uses sensible defaults for rapid development. |
| Boilerplate Code       | Developers often need to write a significant amount of boilerplate code for setting up various components and configurations. | Reduces boilerplate code through auto-configuration, allowing developers to focus more on application logic. |
| Deployment                | Typically, you need to deploy to an external web server, such as Tomcat or Jetty. | Includes support for embedded servers like Tomcat, Jetty, and Undertow, simplifying deployment and testing. |
| Microservices            | Suitable for building microservices but may require additional configuration for each microservice. | Especially well-suited for developing microservices with minimal configuration, making it a popular choice for microservices architecture. |
| Learning Curve        | May have a steeper learning curve due to its extensive features and configuration options. | Easier for developers to get started with, making it more approachable, especially for beginners. |
| Project Structure     | Developers need to define project structures and dependencies explicitly. | Promotes a predefined project structure, and dependencies are automatically managed using "starters." |
| Customization           | Provides extensive customization and flexibility for various components. | Encourages convention-based configuration but allows customization when needed. |
| Community              | Benefits from a large and active community. | Gaining popularity, with a growing community and support. |
| Use Cases               | Suitable for both small and large applications, with flexibility for customization. | Ideal for building microservices and stand-alone applications quickly, making it well-suited for modern development. |


29. **What is the purpose of the Spring Boot embedded server?**
    - Spring Boot embedded servers simplify application deployment.
    - They provide self-contained, standalone runtime environments.


30. **What are the different types of embedded servers supported by Spring Boot?**
    - Spring Boot supports embedded servers like Tomcat, Jetty, and Undertow.
    - You can choose the one that fits your application's requirements.

    
31. **What is the purpose of the application.properties file in Spring Boot?**
    - The `application.properties` file in Spring Boot is used for configuring application properties.
    - It provides a central location to customize settings like database connections, logging, and more.


32. **What is Spring Boot CLI, and how is it used?**
    - Spring Boot CLI is a command-line tool for quickly developing Spring Boot applications.
    - It allows you to write, test, and run Groovy-based Spring applications.


33. **What is Spring Boot Test, and how is it used?**
    - Spring Boot Test provides testing utilities and annotations.
    - It simplifies unit and integration testing of Spring Boot applications.


34. **What is the purpose of the Spring Boot DevTools module?**
    - Spring Boot DevTools is a development-time module for faster application restarts.
    - It offers enhanced development tools and a smoother development experience.


35. **What is the difference between a Spring Bean and a Java object?**
    - A Spring Bean is a Java object managed by the Spring container.
    - Java objects, in general, refer to instances of classes created during application runtime.

| Aspect                        | Spring Bean                                            | Java Object                                        |
|-------------------------------|---------------------------------------------------------|----------------------------------------------------|
| Lifecycle Management        | Managed by the Spring container, allowing for lifecycle control, including initialization and destruction. | Created, initialized, and cleaned up by the developer within the application code. |
| Dependency Injection        | Can be injected with dependencies using Spring's IoC container, simplifying the wiring of components. | Dependencies need to be managed manually through direct instantiation and assignment. |
| Configuration               | Typically configured using Spring's XML or Java-based configuration, making it more flexible and externalized. | Configuration is embedded within the application code, potentially making it less flexible and harder to change. |
| Scopes                        | Can have various scopes, including singleton (default), prototype, request, session, etc., making it versatile. | Typically have a single instance per object instantiation, but this can vary based on how they are created. |
| Testing                       | Easier to create mock or test instances of Spring Beans for unit testing using Spring testing utilities. | Creating mock objects can be more challenging and may require custom test classes or libraries. |
| Reusability                | Encourages reuse and modularity by facilitating the use of beans across different parts of the application. | Limited reusability as objects are usually confined to the part of the application where they are created. |
| Dependency Management | Spring manages dependencies, ensuring that they are available for injection and supporting aspects like AOP. | Developers need to manually handle dependencies and may not benefit from built-in aspects. |
| Decoupling                | Promotes loose coupling as beans depend on abstractions, and dependency injection ensures that specific implementations can be easily swapped. | May lead to tighter coupling if dependencies are directly instantiated within the code. |
| Configuration Changes  | Allows for configuration changes without modifying the source code, making it more maintainable. | Requires code changes to modify configurations, which can be less flexible in some scenarios. |


36. **What is eager loading and lazy loading in the context of software development?**
    - Eager loading retrieves data in advance, which may lead to performance overhead.
    - Lazy loading defers data retrieval until it's needed, potentially improving efficiency.


37. **What are the advantages of using eager loading?**
    - Eager loading reduces the number of queries and enhances initial response times.
    - It simplifies coding and may be suitable when data volumes are manageable.



## Annotations interviews Questions


1. **What is the purpose of the `@SpringBootApplication` annotation in Spring Boot?**
    - The `@SpringBootApplication` annotation in Spring Boot is used to declare a class as a Spring Boot application. It combines three other annotations (`@Configuration`, `@ComponentScan`, and `@EnableAutoConfiguration`) to provide a convenient way to bootstrap a Spring Boot application.


2. **What is the difference between `@Component`, `@Service`, and `@Repository` annotations in Spring Boot?**
    - `@Component`: This is a generic stereotype annotation for any Spring-managed component.
    - `@Service`: It's a specialization of `@Component` used for service classes.
    - `@Repository`: Also a specialization of `@Component`, it's specifically used for database-related classes, enabling Spring's exception translation mechanism.

| Annotation     | Purpose                                                         |
|----------------|-----------------------------------------------------------------|
| `@Component`   | A generic stereotype annotation for any Spring-managed component. |
| `@Service`     | A specialization of `@Component` for service classes.           |
| `@Repository`  | A specialization of `@Component` for database-related classes, specifically for enabling Spring's exception translation mechanism.   |


3. **What is the `@Autowired` annotation and how is it used in Spring Boot?**
    - The `@Autowired` annotation in Spring Boot is used for automatic dependency injection. 
    - It injects dependencies into a Spring Bean, eliminating the need for manual configuration.


4. **How do you use the `@Value` annotation in Spring Boot to inject property values?**
    - The `@Value` annotation in Spring Boot is used to inject property values from property files or environment variables into Spring Beans.


5. **What is the `@RestController` annotation and how is it used in Spring Boot?**
    - The `@RestController` annotation in Spring Boot is a specialization of `@Controller`. 
    - It's used to indicate that a class defines a RESTful web service, allowing the response to be directly returned as JSON or XML.


6. **What is the `@RequestMapping` annotation and how is it used in Spring Boot?**
    - The `@RequestMapping` annotation in Spring Boot is used to map HTTP requests to specific controller methods. 
    - It specifies the URL paths that trigger the corresponding method.


7. **How do you use the `@PathVariable` annotation in Spring Boot to handle dynamic URLs?**
    - The `@PathVariable` annotation in Spring Boot is used to extract values from the URI template and inject them into a method parameter. 
    - It is useful for handling dynamic parts of the URL.


8. **What is the purpose of the `@Configuration` annotation in Spring Boot?**
    - The `@Configuration` annotation in Spring Boot is used to define a class as a source of bean definitions. 
    - It is often used to configure beans for the Spring application context.


9. **What is the `@EnableAutoConfiguration` annotation in Spring Boot and how does it work?**
    - The `@EnableAutoConfiguration` annotation in Spring Boot enables automatic configuration of the Spring application context based on the dependencies and project's classpath.


10. **How do you use the `@Profile` annotation in Spring Boot to create different configurations for different environments?**
    - The `@Profile` annotation in Spring Boot allows you to create different configurations for different environments or application profiles. 
    - It helps specify which beans should be active based on the chosen profile.


11. **What is the difference between `@Controller` and `@RestController`?**
    - `@Controller`: It is a core annotation in Spring MVC and is used to create web application controllers. The methods in a `@Controller` class return view names or model and view objects.
    - `@RestController`: It is a specialized version of `@Controller` designed for RESTful web services. The methods in a `@RestController` return data directly as HTTP response, typically in JSON or XML format.

| Aspect                   | `@Controller`                          | `@RestController`                                      |
|-------------------------|-----------------------------------|-------------------------------------------------------|
| Response Type           | Typically returns a view name or a model and view object. | Returns data directly as HTTP response (e.g., JSON or XML). |
| Purpose                 | Primarily used for traditional web applications.   | Designed for building RESTful web services and APIs.   |
| Common Use Case         | Rendering HTML pages.                | Returning data in response to RESTful requests.        |


12. **What is the difference between `@RequestParam` and `@PathVariable`?**
    - `@RequestParam`: It is used to extract query parameters from the URL. These parameters are usually in the form of `?key=value` and are not part of the URL path.
    - `@PathVariable`: It is used to extract values from the URI template and is typically used for dynamic parts of the URL path.

| Aspect                   | `@RequestParam`                       | `@PathVariable`                    |
|-------------------------|-----------------------------------|-----------------------------------|
| Usage                   | Extracts query parameters from the URL.                | Extracts values from the URI template (URL path).    |
| Syntax                  | Used to handle query parameters and form data.          | Handles dynamic parts of the URL path.               |
| Example URL             | `http://example.com/resource?key=value`               | `http://example.com/resource/{dynamicValue}`        |
| Usage Example           | `@RequestParam String key`                              | `@PathVariable String dynamicValue`                 |
| HTTP Method             | Typically used with `GET` or `POST` requests.          | Commonly used with `GET` requests, especially for RESTful APIs. |


13. **What is the difference between `@Autowired` and `@Inject`?**
   - `@Autowired`: It is a Spring-specific annotation used for automatic dependency injection.
   - `@Inject`: It is part of the Java Dependency Injection (JSR-330) specification and serves the same purpose as `@Autowired`. However, `@Inject` is not Spring-specific and can be used in any framework that supports JSR-330.

| Aspect                   | `@Autowired`                          | `@Inject`                             |
|-------------------------|-----------------------------------|---------------------------------------|
| Origin                  | Spring-specific annotation.        | Part of Java Dependency Injection (JSR-330) specification. |
| Framework               | Works only with Spring Framework.  | Can be used in any framework or context supporting JSR-330. |
| Configuration           | Requires Spring Framework's configuration. | Does not require Spring-specific configuration. |
| Usage                   | Mainly used in Spring applications for dependency injection. | More generic and can be used across various DI frameworks. |


14. **What is the difference between `@GetMapping` and `@PostMapping` in Spring Boot?**
   - `@GetMapping`: It is used to handle HTTP GET requests and is typically associated with read-only operations.
   - `@PostMapping`: It is used to handle HTTP POST requests and is typically associated with data submission or creating resources on the server.

| Aspect                   | `@GetMapping`                        | `@PostMapping`                         |
|-------------------------|-----------------------------------|---------------------------------------|
| HTTP Method             | Specifically for handling HTTP GET requests. | Specifically for handling HTTP POST requests. |
| Use Case                | Typically used for read-only operations, like retrieving data. | Used for operations that create or submit data, such as form submissions. |
| Request Data            | Expects data to be in the query parameters or the request URL. | Expects data to be in the request body, often in the form of submitted data. |
| Idempotent              | Designed for idempotent operations, meaning repeated requests yield the same result. | Not necessarily idempotent; repeated requests may lead to different outcomes. |
| Example Annotation      | `@GetMapping("/resource/{id}")`       | `@PostMapping("/create")`             |
| Example URL             | `http://example.com/resource/123`    | `http://example.com/create`           |


15. **What is the purpose of the `@RestController` annotation in Spring Boot?**
   - The `@RestController` annotation in Spring Boot is a specialization of `@Controller` and is used to indicate that a class defines a RESTful web service. 
   - It allows the response to be directly returned as JSON or XML, making it suitable for building RESTful APIs.


16. **What is the purpose of the `@RequestBody` annotation in Spring Boot?**
   - The `@RequestBody` annotation in Spring Boot is used to indicate that a method parameter should be bound to the body of the HTTP request. 
   - It is commonly used to receive and parse data from POST or PUT requests.


17. **What is the purpose of the `@ResponseBody` annotation in Spring Boot?**
   - The `@ResponseBody` annotation in Spring Boot is used to indicate that the return value of a method should be bound to the body of the HTTP response. 
   - It is typically used in combination with `@Controller` or `@RestController` to send data directly as an HTTP response.


18. **What is the purpose of the `@Valid` annotation in Spring Boot?**
   - The `@Valid` annotation in Spring Boot is used to trigger validation of the annotated object, typically a form object or request payload. 
   - It is often used in combination with validation frameworks like Hibernate Validator.


19. **What is the purpose of `@Autowired` annotation in Spring?**
    - The `@Autowired` annotation in Spring is used for automatic dependency injection. It allows Spring to automatically resolve and inject the required dependencies into a Spring Bean, reducing the need for manual configuration.

20. **List of SpringBoot Annotations**

| Annotation            | Description                                                 |
|-----------------------|-------------------------------------------------------------|
| `@SpringBootApplication` | Indicates the main class of a Spring Boot application. It combines `@Configuration`, `@ComponentScan`, and `@EnableAutoConfiguration`. |
| `@Controller`         | Marks a class as a Spring MVC controller that handles HTTP requests and returns view templates or data. |
| `@RestController`     | Specialization of `@Controller` for building RESTful web services. It returns data directly as HTTP responses (e.g., JSON or XML). |
| `@RequestMapping`      | Maps HTTP requests to specific controller methods and defines the URL paths that trigger the methods. |
| `@GetMapping`          | A specialized form of `@RequestMapping` for handling HTTP GET requests. |
| `@PostMapping`         | A specialized form of `@RequestMapping` for handling HTTP POST requests. |
| `@PutMapping`         | A specialized form of `@RequestMapping` for handling HTTP PUT requests. |
| `@DeleteMapping`      | A specialized form of `@RequestMapping` for handling HTTP DELETE requests. |
| `@RequestParam`        | Binds query parameters or form data to controller method parameters. |
| `@PathVariable`        | Extracts values from the URI template (URL path) and maps them to method parameters. |
| `@RequestBody`         | Binds the request body to a method parameter, typically used for consuming JSON or XML data. |
| `@ResponseBody`        | Indicates that a method's return value should be serialized and returned as the HTTP response body. |
| `@Valid`              | Used to perform validation on the annotated method or argument, commonly used for validating form inputs. |
| `@Value`              | Injects values from property files or environment variables into Spring Beans. |
| `@Autowired`           | Performs automatic dependency injection, injecting dependencies into a Spring Bean. |
| `@Service`            | Specialization of `@Component` for service classes. |
| `@Repository`         | Specialization of `@Component` for database-related classes, specifically for enabling Spring's exception translation mechanism. |
| `@Configuration`      | Specifies that a class is a source of bean definitions, often used to configure beans for the Spring application context. |
| `@EnableAutoConfiguration` | Enables automatic configuration of the Spring application context based on classpath dependencies. |
| `@ComponentScan`      | Scans for Spring-managed components (e.g., beans, services) within a specified base package. |

