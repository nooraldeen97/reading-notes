# Spring Security overview

## Authentication and Access Control
1- Spring Security has an architecture that is designed to separate authentication from authorization and has <br>strategies and extension points for both.

2- Authentication

* An AuthenticationManager can do one of 3 things in its authenticate() method:
* Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.
* Throw an AuthenticationException if it believes that the input represents an invalid principal.
* Return null if it cannot decide.
* An AuthenticationProvider is a bit like an AuthenticationManager, but it has an extra method to allow the caller to query whether it supports a given Authentication type
* An AuthenticationManager hierarchy using ProviderManager

![image](https://github.com/spring-guides/top-spring-security-architecture/raw/main/images/authentication.png)


## Customizing Authentication Managers


* The most commonly used helper is the AuthenticationManagerBuilder: for setting up in-memory, JDBC, or LDAP <br>user details or for adding a custom UserDetailsService<br>
* In a Spring Boot application, you can @Autowired the global one into another bean, but you cannot do that <br>with the local one unless you explicitly expose it yourself.<br>
* Spring Boot provides a default global AuthenticationManager (with only one user) unless you pre-empt it by * <br>providing your own bean of type AuthenticationManager<br>


## Authorization or Access Control

* the core strategy for authorization is AccessDecisionManager<br>
* An AccessDecisionVoter considers an Authentication (representing a principal) and a secure Object, which has been decorated with ConfigAttributes<br>
* Object represents anything that a user might want to access (a web resource or a method in a Java class are the two most common cases).<br>
* Most people use the default AccessDecisionManager, which is AffirmativeBased (if any voters return <br>affirmatively, access is granted).<br>

## Web Security

* Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters<br>

![image](https://github.com/spring-guides/top-spring-security-architecture/raw/main/images/security-filters.png)

* a filter can veto the rest of the chain if it wants to handle the request itself. A filter can also modify <br>the request or the response used in the downstream filters and servlet <br>
* The order of the filter chain is very important, and Spring Boot manages it through two mechanisms<br>
* `@Beans` of type Filter can have an @Order or implement Ordered, and they can be part of a <br>FilterRegistrationBean that itself has an order as part of its API.<br>
* A vanilla Spring Boot application with no custom security configuration has a several (call it n) filter <br>chains, where usually n=6.<br>

**Creating and Customizing Filter Chains**<br>

**Request Matching for Dispatch and Authorization**<br>

## Spring Auth cheat sheet<br>

Step 1: set up a user model and repo<br>
Step 2: create a controller for that model<br>
Step 3: UserDetailsServiceImpl implements UserDetailsService<br>
Step 4: ApplicationUser implements UserDetails<br>
Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter<br>
Step 6: registration page<br>
Step 7: login page<br>