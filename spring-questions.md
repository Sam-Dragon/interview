Spring Interview Questions

1. Can you run a spring application without using @SpringBootApplication <br>
A. Yes, using three annotations [ @Configuration, @EnableAutoConfiguration, @ComponentScan]

2. What is @Configuration <br>

3. What is @EnableAutoConfiguration <br>

4. What is @ComponentScan <br>
A. In order to include external packages [outside the classpath], it works in conjuction with @Component if class

5. What is @RestController <br>
A. It is process of reciving request from front controller registered on class path & default response of [HttpMessageConverter - Jackson] json will provided [@Controller + @ResponseBody] 

6. What is @RequestMapping <br>
A. It is responsible to mapping the incoming request and serve if matches. It is applicable at controller level [root context] or api lelvel [endpoint]
   Basically indicates a resource. Ex. @RequestMapping("/hello") --> http://context:port/resource[hello]

7. How do you support multi-format output for specific endpoint
A. 

8. How to change the response format of api
A. 

9. How to support multiple db
A. 

10. How is serilization working in spring boot ? 
A. Spring boot normally uses JSON library Jackson to serialize and deserialize the objects
