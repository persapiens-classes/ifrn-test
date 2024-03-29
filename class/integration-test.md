Integration Test
====

> [**Integration testing** Integration testing (sometimes called integration and testing, abbreviated I&T) is the phase in software testing in which individual software modules are combined and tested as a group. Integration testing is conducted to evaluate the compliance of a system or component with specified functional requirements.[1] It occurs after unit testing and before system testing.](https://en.wikipedia.org/wiki/Integration_testing) 

## Persistence Layer ##

First of all, review [Persistence Layer](persistence-layer.md).

## :star: Integration testing match with Persistence Layer ##

[Baeldung post](https://www.baeldung.com/spring-boot-testing) is a good start to understand Spring Boot Testing.

### Activate integration tests at pom
```xml
    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-failsafe-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
```

### See Integration classes 

- Class with IT extension

- Class with @SpringBootTest annotation

- Methods with @Test annotation

### See factory classes that help creating testing scenarios

- Factory Classes with @Component annotation

- Test Class with @Autowired annotation on attributes

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/issues/134)

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

Implement integration tests for **crud (create/retrieve/update/delete)** crud methods of two repositories of your domain classes.

Create a **separate commit** to each repository integration test of your domain classes.
