Persistence Annotations on Domain Classes
====

We will use [Hibernate](https://www.hibernate.org) and [Jakarta JPA specifications](https://jakarta.ee/specifications/persistence/) to work with Persistence Annotations on domain classes.

See full [Hibernate Reference Documentation](https://docs.jboss.org/hibernate/orm/6.2/userguide/html_single/Hibernate_User_Guide.html#domain-model) when you need additional information.


# Class Annotations

- @Entity
- @Inheritance

## Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

# Attribute Annotations

- @ID
- @Column
- @Temporal

## Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

# Association Annotations

- @JoinCoumn
- @ManyToOne
- @OneToMany
- @ManyToMany
- @OneToOne

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/dominio)

## Create Schema using Spring Data And JPA ##

Using [Baeldung post](https://www.baeldung.com/spring-data-jpa-generate-db-schema) to extract the following steps:

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

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/resources/application.yml)

# :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

Annotate your domain classes with persistence class annotations.

Annotate your domain classes with persistence attribute annotations.

Annotate your domain classes with persistence relationship annotations.

Create the schema create and drop scripts of your database from your domain classes.

Create a **separate commit** to each step of this activity.

