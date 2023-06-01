Persistence Repositories of Domain Classes
====

We will use [Spring Data JPA](https://spring.io/projects/spring-data-jpa) to create persistence repositories of domain classes.

See full [Spring Data JPA Reference Documentation](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.repositories) when you need additional information.

# Using Repositories Interfaces

```
public interface CategoriaRepository extends        CrudRepository<Categoria, Long> {
}
```


# Using Repositories Interfaces with Query Methods

```
public interface ValorInicialDoDonoNaContaPatrimonioRepository extends CrudRepository<ValorInicialDoDonoNaContaPatrimonio, Long> {
    
  ValorInicialDoDonoNaContaPatrimonio findByDonoAndContaPatrimonio(Dono dono, ContaPatrimonio contaPatrimonio);
    
}
```

# Using Query By Example

```
public interface ContaCreditoRepository extends CrudRepository<ContaCredito, Long>, QueryByExampleExecutor<ContaCredito> {
}
```


## Hands on with [Conta Example Project.](https://github.com/persapiens/conta/tree/main/src/main/java/br/edu/ifrn/conta/persistencia)
