# Spring Auth

## Spring Auth Cheat Sheet

1 Set up a user model and repo

2 create a controller for that model

3  UserDetailsServiceImpl implements UserDetailsService

4 ApplicationUser implements UserDetails

5 WebSecurityConfig extends WebSecurityConfigurerAdapter

6 Set up registration page with a form

7 Create log in page with a form


# Spring Authorization

Using GitHub for authentication.

```java
<dependency> //Dependency to add for OAuth 2.0
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>
```

Add a [github app](https://github.com/settings/developers) by selecting for a new app and then register a new app with a name a description and the app's home page, or the localhost the app is hosted on. Use `http://localhost:8080/login/oauth2/code/github` as the authorization callback url and register.

```java
spring:             // Add to application.yml
  security:
    oauth2:
      client:
        registration:
          github:
            clientId: github-client-id       // replace with credentials from github
            clientSecret: github-client-secret        // replace with credentials from github
# ...
```

In launching the app homepage it should redirect to a github login.



## Web Security

 * Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters .


* The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.


* Spring Security is installed as a single Filter in the chain, and its concrete type is FilterChainProxy.


* the security filter is a @Bean in the ApplicationContext, and it is installed by default so that it is applied to every request.


* There can be multiple filter chains all managed by Spring Security in the same top level FilterChainProxy and all are unknown to the container.


[<== Back to Readme](README.md)
