Controller Layer
====

- Contains **classes** and **annotations** that are responsible to interact with external users and applications.
- **Dependent** of service and model layer.

# Application Layers #

![Layered Architecture](layered-architecture.png)

This image was extracted from [Layered Architecture article.](https://herbertograca.com/2017/08/03/layered-architecture/")

## Add springdoc

Include [springdoc](https://springdoc.org/v2/) in your application pom.xml.

```xml
    <properties>
        <springdoc.version>2.1.0</springdoc.version>
    </properties>

    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springdoc</groupId>
                <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
                <version>${springdoc.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springdoc</groupId>
                <artifactId>springdoc-openapi-starter-common</artifactId>
                <version>${springdoc.version}</version>
            </dependency>
        </dependencies>
    </dependencyManagement>

    <dependencies> 
        <dependency>
            <groupId>org.springdoc</groupId>
            <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springdoc</groupId>
            <artifactId>springdoc-openapi-starter-common</artifactId>
        </dependency>
    </dependencies> 
```

## Browser api using swagger

1. Run your app

2. Access it with http://localhost:8080/swagger-ui.html

## Create Services

See service package of [conta project](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/service)

Pay attention to CrudService.

Pay attention to saldo method of SaldoService class.

Pay attention to transferir method of TransferenciaService class.

## Create Controllers

See controllers package of [conta project](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/controller)

Pay attention to CrudController.

Pay attention to saldo method of SaldoController class.

Pay attention to transferir method of TransferenciaController class.

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta)

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

1. Implement services and controllers for **crud (create/retrieve/update/delete)** crud methods of two domain classes.

2. Include some api producer like swagger in your app.

Create a **separate commit** to each repository integration test of your domain classes.

