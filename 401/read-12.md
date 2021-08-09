# Spring RESTful Routing & Static Files

## Spring RequestMapping
## @RequestMapping — by Path
`@RequestMapping(value = "/ex/foos", method = RequestMethod.GET) @ResponseBody public String getFoosBySimplePath() { return "Get some Foos"; }`

## @RequestMapping — the HTTP Method
The HTTP method parameter has no default. So, if we don't specify a value, it's going to map to any HTTP request.

`@RequestMapping(value = "/ex/foos", method = POST) @ResponseBody public String postFoos() { return "Post some Foos"; }`

## @RequestMapping Consumes and Produces
Mapping media types produced by a controller method is worth special attention. We can map a request based on its Accept header via the @RequestMapping headers attribute introduced above:

`@RequestMapping( value = "/ex/foos", method = GET, headers = "Accept=application/json") @ResponseBody public String getFoosAsJsonFromBrowser() { return "Get some Foos with Header Old"; }`

When specified at the type level, the method-level annotations do not complement but override the type-level information.

New Request Mapping Shortcuts
Spring Framework 4.3 introduced a few new HTTP mapping annotations, all based on @RequestMapping:

1- @PatchMapping

2- @DeleteMapping

3- @PutMapping

4- @PostMapping

5- @GetMapping


## Create Simple Queries
Spring Data JPA focuses on using JPA to store data in a relational database. Its most compelling feature is the ability to create repository implementations automatically, at runtime, from a repository interface.


## Create an Application Class
@SpringBootApplication is a convenience annotation that adds all of the following:

* @Configuration: Tags the class as a source of bean definitions for the application context.

* @EnableAutoConfiguration: Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings.

* @ComponentScan: Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.


## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data
CrudRepository provides CRUD functions.

PagingAndSortingRepository provides methods to do pagination and sort records.

JpaRepository provides JPA related methods such as flushing the persistence context and delete records in a batch.

Simple Product entity:

`@Entity public class Product {
@Id
private long id;
private String name;
// getters and setters
} `

`{<S extends T> S save(S entity);
T findOne(ID primaryKey);
Iterable<T> findAll();
Long count();
void delete(T entity);
boolean exists(ID primaryKey);}`

## CRUD functionality:

* save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch.

* findOne(…) – get a single entity based on passed primary key value.

* findAll() – get an Iterable of all available entities in database.

* count() – return the count of total entities in a table.

* delete(…) – delete an entity based on the passed object.

* exists(…) – verify if an entity exists based on the passed primary key value.