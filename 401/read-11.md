# Spring App Basics <br>

1- build an application that has a static home page and that will also accept HTTP GET requests<br>
2- It will respond with a web page that displays HTML. The body of the HTML will contain a greeting: “Hello, <br>World!”<br>
3- You can customize the greeting with an optional name parameter in the query string. The URL might then be <br>http://localhost:8080/greeting?name=User<br>
4- Used Spring Initializr to initialize a new spring project<br>
5-In Spring’s approach to building web sites, HTTP requests are handled by a controller @Controller<br>
6- The @GetMapping annotation ensures that HTTP GET requests for example to /greeting are mapped to the greeting<br>() method.<br>
7-@RequestParam binds the value of the query string parameter into the parameter of the greeting() method.<br>
8-This query string parameter is not required. If it is absent in the request, the defaultValue of World is<br> used.<br>
9-@SpringBootApplication is a convenience annotation that adds all of the following:<br>
- @Configuration: Tags the class as a source of bean definitions for the application context.<br>
- @EnableAutoConfiguration: Tells Spring Boot to start adding beans based on classpath settings, other beans,<br> and various property settings.<br>
- @ComponentScan: Tells Spring to look for other components, configurations, and services in the com/example <br>package, letting it find the controllers.<br>
10-The main() method uses Spring Boot’s SpringApplication.run() method to launch an application.<br>

## Build an executable JAR<br>
- Building an executable jar makes it easy to ship, version, and deploy the service as an application<br> throughout the development lifecycle, across different environments, and so forth.<br>

## RUN<br>
- gradle: ./gradlew bootRun<br>
- build the JAR file by using ./gradlew build and then run the JAR file by java -jar target/<br>gs-serving-web-content-0.1.0.jar<br>

## Add a Home Page<br>
- Spring Boot serves static content from resources in the classpath at /static (or /public). The index.html <br>resource is special because, if it exists, it is used as a "`welcome page<br>


# Spring MVC and Thymeleaf<br>

1-Spring model attributes
Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The<br> equivalent term in Thymeleaf language is context variables.<br>
2-How to add model attributes to a view in Spring MVC<br>
- Add attribute to Model via its addAttribute method:<br>
- Return ModelAndView with model attributes included:<br>
- Expose common attributes via methods annotated with @ModelAttribute:<br>
3-You can access model attributes in views with Thymeleaf as follows:<br>

`<tr th:each="message : ${messages}">`<br>
    `<td th:text="${message.id}">1</td>`<br>
    `<td>`<br>
        `<a href="#" th:text="${message.title}">Title ...</a>`<br>
    `</td>`<br>
    `<td th:text="${message.text}">Text ...</td>`<br>
`</tr>` <br>

## Request parameters<br>
* In order to access the q parameter in `https://example.com/query?q=Thymeleaf+Is+Great!` you can use the param <br>prefix `<p th:text="${param.q}">Test</p>`<br>
* If you access multivalued parameter with ${param.q} you will get a serialized array as a value.<br>

## Session attributes<br>
* Similarly to the request parameters, session attributes can be accessed by using the session. prefix <br>`<p th:text="${session.mySessionAttribute}" th:unless="${session == null}">[...]</p>`<br>

## ServletContext attributes<br>
* In order to access ServletContext attributes in Thymeleaf you can use the #servletContext. prefix<br>

## Spring beans<br>
* Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax<br>
@urlService refers to a Spring Bean registered at your context `<div th:text="${@urlService.getApplicationUrl()}">...</div>`<br>


