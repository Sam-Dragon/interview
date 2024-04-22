Spring Interview Questions

1. Can you run a spring application without using @SpringBootApplication <br>
- Yes, using three annotations [ @Configuration, @EnableAutoConfiguration, @ComponentScan]

2. What is @Configuration

3. What is @EnableAutoConfiguration

4. What is @ComponentScan
A. In order to include external packages [outside the classpath], it works in conjuction with @Component if class

5. What is @RestController
A. It is process of reciving request from front controller registered on class path & default response of [HttpMessageConverter - Jackson] json will provided  
   [ @Controller + @ResponseBody ] 

5. What is @RequestMapping
A. It is responsible to mapping the incoming request and serve if matches.
   Basically indicates a resource. Ex. @RequestMapping("/hello") --> http://context:port/resource[hello]
