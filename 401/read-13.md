# Related Resources and Integration Testing
## Related data in Spring
## One-to-One Relationship
- `@OneToOne...@JoinColumn(name = "address_id"), @OneToOne(mappedBy = "address")`

- We must be careful to have different names for each association resource. Otherwise, we will encounter a JsonMappingException

- create two repository interfaces for each of them, by extending the CrudRepository interface

## One-to-Many Relationship
- example: there are many books in the library
- A one-to-many relationship is defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.
- create two repository interfaces for each of them, by extending the CrudRepository interface

## Many-to-Many Relationship
- example there are many authors for many books
- A many-to-many relationship is defined using @ManyToMany annotation, to which we can add @RestResource.
- create two repository interfaces for each of them, by extending the CrudRepository interface

## Baeldung: Spring Integration Testing

## Enable Spring in Tests with JUnit 5

- We can enable this extension by adding the @ExtendWith annotation to our test classes and specifying the extension class to load. To run the Spring test, we use SpringExtension.class.
- We also need the @ContextConfiguration annotation to load the context configuration and bootstrap the context that our test will use.
- Finally, we also annotate the test with @WebAppConfiguration, which will load the web application context.

## The WebApplicationContext Object
- WebApplicationContext provides a web application configuration. It loads all the application beans and controllers into the context.

## Mocking Web Context Beans

- MockMvc provides support for Spring MVC testing. It encapsulates all web application beans and makes them available for testing.

## Verify Test Configuration
## Writing Integration Tests

**Verify View Name**

- perform() method will call a GET request method, which returns the ResultActions. Using this result, we can have assertion expectations about the response, like its content, HTTP status, or header
- andDo(print()) will print the request and response. This is helpful to get a detailed view in case of an error
- andExpect() will expect the provided argument. In our case, we're expecting “index” to be returned via MockMvcResultMatchers.view()

**Verify Response Body**

andExpect(MockMvcResultMatchers.status().isOk()) will verify that response HTTP status is Ok (200).
andExpect(MockMvcResultMatchers.jsonPath(“$.message”).value(“Hello World!!!”)) will verify that response content matches with the argument “Hello World!!!“.
andReturn() will return the MvcResult object, which is used when we have to verify something that isn't directly achievable by the library. In this case, we've added assertEquals to match the content type of the response that is extracted from the MvcResult object

**Send GET Request With Path Variable**

* MockMvcRequestBuilders.get(“/greetWithPathVariable/{name}”, “John”) will send a request as “/greetWithPathVariable/John“.
**Send GET Request With Query Parameters**

* param(“name”, “John Doe”) will append the query parameter in the GET request. This is similar to “/greetWithQueryVariable?name=John%20Doe“.

**Send POST Request**

* MockMvcRequestBuilders.post(“/greetWithPost”) will send the POST request. We can set path variables and query parameters in a similar way as before, whereas form data can be set only via the param() method, similar to query parameters

## MockMvc Limitations
* The MockMvc class wraps this TestDispatcherServlet internally. So, every time we send a request using the perform() method, MockMvc will use the underlying TestDispatcherServlet directly. Therefore, there are no real network connections made, and consequently, we won't test the whole network stack while using MockMvc.
* because Spring prepares a fake web application context to mock the HTTP requests and responses, it may not support all features of a full-blown Spring application.