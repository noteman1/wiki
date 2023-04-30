application.yml
```yml
spring:
  mvc:
    pathmatch:
      matching-strategy: ant_path_matcher
```

build.gradle
```gradle
dependencies {
    implementation 'io.springfox:springfox-boot-starter:3.0.0'
    implementation 'io.springfox:springfox-swagger-ui:3.0.0'
}
```

configuration/SwaggerConfiguration.java
```java
@Configuration
public class SwaggerConfiguration {
    @Bean
    public Docket api() {
        return new Docket(DocumentationType.OAS_30)
                .apiInfo(apiInfo())
                .select()
                .apis(RequestHandlerSelectors.any())
                .paths(PathSelectors.any())
                .build();
    }
    
    
    public ApiInfo apiInfo() {
        return new ApiInfoBuilder()
                .title("Rest API Documentation")
                .description("Rest API Documentation")
                .version("0.1")
                .build();
    }   
}
```

```sh
open http://localhost:8080/swagger-ui/index.html
```