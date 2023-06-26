System Test
====

> [**System testing** System testing is a type of software testing that evaluates the overall functionality and performance of a complete and fully integrated software solution. It tests if the system meets the specified requirements and if it is suitable for delivery to the end-users. This type of testing is performed after the integration testing and before the acceptance testing.](https://www.geeksforgeeks.org/system-testing/) 

## Controller Layer ##

1. First of all, review [Controller Layer](controller-layer.md).

2. Now, [See detailed Application Layer explanation class.](application-layers.md)

## :star: System testing match with Controller Layer ##

[Baeldung post](https://www.baeldung.com/spring-boot-testing) is a good start to understand Spring Boot Testing.

### See System Test classes 

- Class with IT extension

- Class with @SpringBootTest annotation

- Methods with @Test annotation

- RestClient classes are rest json api client of controllers.

### See factory classes that help creating testing scenarios

- Factory Classes with @Component annotation

- Test Class with @Autowired annotation on attributes

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/issues/134)

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

Implement system tests for **crud (create/retrieve/update/delete)** crud methods of two domain classes.

Create a **separate commit** to each system test of your domain classes.
