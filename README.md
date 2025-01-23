The project was initially generated on https://start.spring.io/.
The manual was provided in the email so in this note i will focus on the understanding of the code.

  ![image](https://github.com/user-attachments/assets/35c54992-9258-45fc-bb4d-28b067ba57d5)

  
  
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;1   

These lines above import necessary classes from the Spring Boot framework.



Controller -> indicates that the class HelloController is a Spring MVC controller. Controllers handle incoming HTTP requests and are responsible for coordinating application logic and responses.

Model -> is used to hold data that will be passed to the template view.

GetMapping ->  is used to map a request method (GET in this case) to a specific handler method within the controller.

RequestParam -> is used to handle request parameters sent along with the GET request.

@Controller ->  marks the class HelloController as a Spring MVC controller.

The project is launched on the localhost:8080

hello() -> this method is a request handler that is invoked when a GET request is made to the root path (/). It returns a string message "Hello Vistula, in my first Spring controller". This string will likely be used as the content of a web page.

greeting(String name, Model model) -> this method is another request handler, invoked when a GET request is made to the path /greeting.

String name -> this argument captures the value of the name parameter sent along with the request. It has a default value of "World" if no name is provided.
Model model -> this argument is an instance of the Model class used to store data that will be passed to the template view.

http://localhost:8080/greeting?name=Vistula is an example URL that would invoke the greeting - the look of the website was modified accordingly in the html file shows below:

![image](https://github.com/user-attachments/assets/16dbd627-9ba0-46d8-8433-24283472558a)


and the final result of website http://localhost:8080/greeting?name=Vistula looks like this:

![image](https://github.com/user-attachments/assets/12949bd8-6e4c-4271-bdca-543afe854c27)



