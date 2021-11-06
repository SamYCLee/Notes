# Spring Boot Annotation

## Annotation

### **@SpringBootApplication**

`@SpringBootApplication` is the annotation that defaults to be shown at the main function when using the Spring Initializer to initialize a project. It is equivalent to use all `@Configuration`, `@EnableAutoConfiguration` and `@ComponentScan`.

    @SpringBootApplication
    public class Application {

      public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
      }

    }
