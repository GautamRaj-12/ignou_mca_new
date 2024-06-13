# Introduction to Spring Boot

## Limitations of Spring that led to the development of Spring Boot

- Spring based application requires *many configurations* and *complicated dependency management*. So, the setup is very *tedious* and *error prone*
- Some repetition of same configuration steps:
  - Import the **required dependecies** like *spring mvc*,*spring jpa*,*spring jdbc*,*spring rest*
  - Import the **specified spring version** compatible *third party libraries* such as *hibernate*, *jackson* etc
  - **Configure web layer beans** such as *view resolver*,*resourcce manager*
  - **Configure DAO layers** such as *data source*, *transaction management*, *entity manager*
  - **Import web containers** in the case of web applications.

## Spring Boot
- Spring Boot is a an extension of Spring framework which **enables an organization to develop production-ready spring-based applications** and services with *less effort*, *reduced cost* and *minimal configuration*. It provides *auto-configuration* which reduces the number of lines of code significantly.
- It eliminates the **boilerplate configuration required** for a spring application.It is a module that enriches the Spring framework with **Rapid Application Development(RAD)** feature.
- It is a combination of Spring Framework with **auto-configuration** and **embedded servers**.

## Features and Benefits of Spring Boot
- Everything is **auto-configured** in Spring Boot.
- Spring Boot starter **eases the dependency management** and application 
**configuration** 
- It **simplifies the application deployment** by **using an embedded server** 
- Production ready **features to monitor and manage applications**, such as health 
checks, metrics gathering etc. 
- **Reduces the application development time** and run the application 
independently 
- Very easy to understand and develop Spring application 
- **Increases productivity** and **reduces the cost** 

## Spring Boot working and annotations
- ***ENTRY POINT***:A class with the **main method** and annotated with **@SpringBootApplication** is the entry point of the Spring Boot application. 

![spring boot app entry point](images/springbootapp.png)

- Spring Boot **auto-configures** all required configurations.
- It performs auto-configuration by scanning the classes in class-path annotated with **@Component** or **@Configuration**. 
- The **@SpringBootApplication** annotation is a convenient annotation that combines three essential annotations for a Spring Boot application:
  - **@EnableAutoConfiguration**
  - **@ComponentScan**
  - **@Configuration**

### @EnableAutoConfiguration
This annotation tells Spring Boot to automatically configure your application based on the dependencies present in the classpath.

- For example, if you have `spring-boot-starter-web` in your dependencies, Spring Boot will automatically configure the necessary components for a web application, such as a `DispatcherServlet`, view resolvers, etc.
- It works by searching for specific configuration classes (provided by Spring Boot) and applying them to the application context.

### @ComponentScan
This annotation tells Spring to scan the current package and its sub-packages for components, configurations, and services.

- By default, it starts scanning from the package of the class that declares this annotation.
- This is crucial for Spring to detect all the beans and components that you have defined in your application.

### @Configuration
This annotation indicates that the class can be used by the Spring IoC container as a source of bean definitions.

- It is a marker for classes that provide one or more `@Bean` methods.
- These beans will be managed by the Spring container, and their lifecycle will be handled by Spring.

### How It All Comes Together
When you annotate your main application class with `@SpringBootApplication`, you are enabling auto-configuration, component scanning, and configuration in one go. Here's what typically happens:

1. **Auto-Configuration**: Spring Boot tries to automatically configure your application based on the dependencies in the classpath. If `spring-boot-starter-data-jpa` is present, it will set up a DataSource and JPA-related beans.

2. **Component Scanning**: Spring Boot scans the package of the main application class and all its sub-packages for components and configurations. It finds classes annotated with `@Component`, `@Service`, `@Repository`, `@Controller`, and `@Configuration`, and registers them as beans in the application context.

3. **Configuration Classes**: Spring Boot processes classes annotated with `@Configuration` to create beans that may be needed in the application context.

## Spring Boot Conditional Annotations

Spring Boot provides a set of conditional annotations that allow beans to be registered or not based on specific conditions. These conditions are useful for creating more flexible and modular configurations. Here's an explanation of some commonly used conditional annotations:

### @ConditionalOnClass
This annotation is used to conditionally create a bean if a specified class is present on the classpath.

- **Usage**: It is typically used to enable auto-configuration only when certain dependencies are available.
- **Example**:
  ```java
  @ConditionalOnClass(name = "com.example.MyClass")
  public class MyConditionalConfig {
      // Bean definitions
  }
- In this example, the configuration inside MyConditionalConfig will only be applied if com.example.MyClass is present on the classpath.

### @ConditionalOnMissingClass

This annotation is the opposite of `@ConditionalOnClass`. It is used to conditionally create a bean if a specified class is not present on the classpath.

- **Usage**: It is useful when you want to apply a configuration only when a certain dependency is absent.
- **Example**:
  ```java
  @ConditionalOnMissingClass(value = "com.example.MyClass")
  public class MyFallbackConfig {
      // Bean definitions
  }
- Here, the configuration inside MyFallbackConfig will only be applied if com.example.MyClass is not present on the classpath.

### @ConditionalOnBean

This annotation is used to conditionally create a bean if a specified bean is already defined in the Spring context.

- **Usage**: It is often used to create a bean that depends on another bean being present.
- **Example**:
  ```java
  @ConditionalOnBean(name = "myExistingBean")
  public class MyDependentConfig {
      // Bean definitions
  }
- The configuration inside MyDependentConfig will only be applied if a bean named myExistingBean is already defined.

### @ConditionalOnMissingBean

This annotation is the opposite of `@ConditionalOnBean`. It is used to conditionally create a bean if a specified bean is not already defined in the Spring context.

- **Usage**: It is useful for providing default beans that can be overridden by user-defined beans.
- **Example**:
  ```java
  @ConditionalOnMissingBean(name = "myOptionalBean")
  public class MyDefaultConfig {
      // Bean definitions
  }
- In this case, the configuration inside MyDefaultConfig will only be applied if a bean named myOptionalBean is not defined.
  
### @ConditionalOnProperty

This annotation is used to conditionally create a bean based on the value of a specified property.

- **Usage**: It is commonly used to enable or disable parts of the configuration based on properties set in the `application.properties` or `application.yml` file.
- **Example**:
  ```java
  @ConditionalOnProperty(name = "my.feature.enabled", havingValue = "true")
  public class MyFeatureConfig {
      // Bean definitions
  }
- The configuration inside MyFeatureConfig will only be applied if the property my.feature.enabled is set to true.
  
### @ConditionalOnResource

This annotation is used to conditionally create a bean if a specified resource is present on the classpath.

- **Usage**: It is useful for enabling configuration based on the presence of files or other resources.
- **Example**:
  ```java
  @ConditionalOnResource(resources = "classpath:my-resource.txt")
  public class MyResourceConfig {
      // Bean definitions
  }
- Here, the configuration inside MyResourceConfig will only be applied if my-resource.txt is present in the classpath.


## Spring Boot Starter
- Before Spring Boot was introduced, Spring Developers used to spend a lot of time on Dependency management. **Spring Boot Starters** were introduced to solve this problem so that the developers can spend more time on actual code than Dependencies. *Spring Boot Starters are dependency descriptors that can be added under the `<dependencies>` section in pom.xml*. There are around 50+ Spring Boot Starters for different Spring and related technologies. These starters give all the dependencies under a single name.
- For example, if you want to use **Spring Data JPA for database access**, you can include `spring-boot-starter-data-jpa` dependency. 

### Advantages of using starters
- Increase productivity by decreasing the Configuration time for developers.
- Managing the POM is easier since the number of dependencies to be added is decreased.
- Tested, Production-ready, and supported dependency configurations.
- No need to remember the name and version of the dependencies.

Dependencies in pom.xml:
![dependecies in pom.xml](images/dependecies%20in%20pom.xml.png)

| Starter                        | Description                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------|
| `spring-boot-starter-web`      | It is used for building web applications, including RESTful applications using Spring MVC. It uses Tomcat as the default embedded container. |
| `spring-boot-starter-jdbc`     | It is used for JDBC with the Tomcat JDBC connection pool.                                   |
| `spring-boot-starter-validation` | It is used for Java Bean Validation with Hibernate Validator.                              |
| `spring-boot-starter-security` | It is used for Spring Security.                                                             |
| `spring-boot-starter-data-jpa` | It is used for Spring Data JPA with Hibernate.                                              |
| `spring-boot-starter`          | It is used as a core starter, including auto-configuration support, logging etc.            |
| `spring-boot-starter-test`     | It is used to test Spring Boot applications with libraries, including JUnit, Hamcrest, and Mockito. |
| `spring-boot-starter-thymeleaf` | It is used to build MVC web applications using Thymeleaf views.                            |

## Creating a spring boot project

### Requirements

- JDK 17+
- IDE

### Installing JDK

- Download from oracle website. Install using GUI in Windows/Mac/Linux.

### IDE

- **INTELLIJ COMMUNITY**
    - Installation GUI in windows and mac
    - In Linux: https://www.jetbrains.com/idea/download/?section=linux
    
    ```bash
    sudo snap install intellij-idea-community --classic
    ```
    
    or download tar file and extract and install.
    

### Intellij Community version doesn’t have web features

- So we need to find a way to run web frameworks in community edition.
- Go to https://start.spring.io/ - It allows us to configure and then download a skeleton spring boot project

### Spring Initializer Configuration

- The most basic spring web app configuration

![spring-initializer](images/spring-initializer.png)

- Click on generate - A zip file will be downloaded
- Extract and Open it in intellij.
- The setup is done.

## Spring Boot Project Structure
- After opening the configured project in intellij. The directory structure would be like this:
![spring boot directory structure](images/spring-boot-directory-structure.png)

- The **@SpringBootApplication** annotation triggers component scanning for the current package and its sub-packages. Therefore, the main class of the project should reside in the base package to use the implicit components scan of spring boot.

## Writing First Controller
- Go to ***src → main → java → com.gautam.legalblogs(your group)*** and create a class.
- Example ***HelloWorldController.java***

  ![creating class](images/creating-class.png)
  ![created class](images/created-class.png)

- Default code in the class
  ![default code](images/default-code.png)

- Wrting a basic controller
  ![basic controller](images/controller.png)


## RUNNING OUR APP

- ***src → main → java → LegalblogsApplication → right click →run***
  ![running](images/running.png)

- Output
  ![output](images/running-2.png)

- If port 8080 is busy, then you have to configure this to run on different port, or stop the service running on port 8080

- Now, go to your browser and type ***http://localhost:8080/hello*** in the url bar.
- You should be able to see the following screen  

![Localhost](images/localhost.png)

## Spring Boot Runners
- Runners let you to execute the code after the Spring Boot application is started. You can use these interfaces to perform any actions immediately after the application has started.
- Spring boot provides two runner interfaces:
    1. **Application Runner**
    2. **Command Line Runner**

### 1. Application Runner
- Application Runner is an interface used to execute the code after the Spring Boot application started. The example given below shows how to implement the Application Runner interface on the main class file.
```
package com.tutorialspoint.demo;

import org.springframework.boot.ApplicationArguments;
import org.springframework.boot.ApplicationRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication implements ApplicationRunner {
   public static void main(String[] args) {
      SpringApplication.run(DemoApplication.class, args);
   }
   @Override
   public void run(ApplicationArguments arg0) throws Exception {
      System.out.println("Hello World from Application Runner");
   }
}
```

### 2. Command Line Runner
- Command Line Runner is an interface. It is used to execute the code after the Spring Boot application started. The example given below shows how to implement the Command Line Runner interface on the main class file.
  
```
package com.tutorialspoint.demo;

import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication implements CommandLineRunner {
   public static void main(String[] args) {
      SpringApplication.run(DemoApplication.class, args);
   }
   @Override
   public void run(String... arg0) throws Exception {
      System.out.println("Hello world from Command Line Runner");
   }
}
```

## Spring Boot Web Application Using Thymeleaf

### Thymeleaf
- Thymeleaf is a server-side Java template engine for both web and standalone environments. Its main goal is to bring natural templates to your development workflow — HTML that can be correctly displayed in browsers and also work as static prototypes.

1. Initialize the project as explained above and open it in intellij.
2. Add a HomeController. HomeController has two endpoints
   - **“/”** 
   - **“/greeting?name=Raj”** 
3. Add thymeleaf dependency in pom.xml and press `ctrl+shift+o' to install the changes.
   ```
   <dependency>
			<groupId>org.thymeleaf</groupId>
			<artifactId>thymeleaf</artifactId>
			<version>3.1.2.RELEASE</version>
		</dependency>
   ```
4. Add the corresponding HTML template file into `src/main/resources/templates`
   - **home.html**
   - **greeting.html**