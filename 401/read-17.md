# Spring Boot and OAuth2
* There are several samples building on each other, adding new features at each step:

* simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties .

* click: adds an explicit link that the user has to click to login.

* logout: adds a logout link as well for authenticated users.

* two-providers: adds a second login provider so the user can choose on the home page which one to use.

* custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

* You can run the main method in SocialApplication to start an app. They all come up with a home page on http://localhost:8080.

* You can also run all the apps on the command line using mvn spring-boot:run or by building the jar file and running it with mvn package and java -jar target/*.jar.



**All of the sample apps can be easily extended and re-configured for more specific use cases, usually with <br>nothing more than a configuration file change. Remember if you use versions of the samples in your own servers to register with GitHub (or similar) and get client credentials for your own host addresses. And  remember not to put those credentials in source control!**<br>