Persistence Layer
====

- Contains **classes** and **annotations** that are responsible to persist domain application classes.
- **Must** be involved with **non-functional requirements** of the application: persistence, transaction isolation.
- **Dependent** of persistence technology.

# Application Layers #

![Layered Architecture](layered-architecture.png)

This image was extracted from [Layered Architecture article.](https://herbertograca.com/2017/08/03/layered-architecture/")

# Persistence Annotations on Domain Classes #

## Class Annotations ##

- @Entity
- @Inheritance

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

## Attribute Annotations ##

- @ID
- @Column
- @Temporal

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

## Association Annotations ##

- @JoinCoumn
- @ManyToOne
- @OneToMany
- @ManyToMany
- @OneToOne

## See full [documentation](https://docs.jboss.org/hibernate/orm/6.2/userguide/html_single/Hibernate_User_Guide.html#domain-model)

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

## Create Schema using Spring Data And JPA ##

- Add Configuration to your application.yml

```
spring:
  jpa:
    properties:
      jakarta:
        persistence:
          schema-generation:
            scripts:
              action: drop-and-create
              create-target: target/create.sql
              drop-target: target/drop.sql
```

- Run your project

Using [Baeldung post](https://www.baeldung.com/spring-data-jpa-generate-db-schema)

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/resources/application.yml)

# :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

Annotate your domain classes with persistence class annotations.

Annotate your domain classes with persistence attribute annotations.

Annotate your domain classes with persistence relationship annotations.

Create the schema create and drop scripts of your database from your domain classes.

Create a **separate commit** to each step of this activity.

# Repository Interfaces and Classes #

- TODO


