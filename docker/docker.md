   # Questions

1. what is docker.? why we use it.? what is required to run docker.? <br>
A. Packing applications with required dependencies and libraries
   - Use: Portability, Fast Bootup, Sharing
   - Advantage: Matrix of hell, Ease of deployment, Compatibility issues

2. where do you store docker images so that it is easily sharable.? <br>
A. Generally it is stored in docker hub registry

3. How many ways can we share docker images to the user.? <br>
A. Generally if you want to share privately, use docker save and load and share the images in zip file
   - If you want to share publically, share it via docker hub registry

4. what is docker image & docker container.? <br>
A. Package template which contains application along with dependencies and libraries
   - Docker container: It is running instance of docker image

5. what is docker volume.? how is it useful.? <br>
A. It is the storage mechanism which will save the data even if docker container is removed or crashed.
   - Data will be available when the container is created

6. How do you share volume b/w multiple applications.? <br>
A.  We can create shared volume and pass it between applications

7. How would you create dummy container to test some functionality.? <br>
A.  Use docker run command with sleep and test the functionality [Dont use in detached mode]

8. How do you copy files inside/outside the container.? <br>
A.  docker cp would be useful for copying files from outside to inside container

9. Lifecycle of docker container ? <br>
A. Following are the stages of docker container
   - Created         :   docker build (OR) docker create (OR) docker run 
   - Running         :   docker run
   - Paused          :   docker pause
   - Stopped/Exited  :   docker stop
   - Removed/Deleted :   docker rm

10. Docker Client Vs Docker Deamon Vs Docker Engine.?  <br>
   - Docker client or docker cli is responsible for accepting all the commands from user and send it to appropritate api
   - Docker Deamon is backend thread which is responsible for executing those commands and return the results
   - Docker Engine = Docker CLI + API's + Docker Deamon

11. What are C-groups in docker ?  <br>
A. To control the amount of hardward / cpu to allocate for docker [option: --cpu or --memory]

12. What are docker network types ? which is default.  <br>
A.  bridge [default], none, host

13. What is embedded DNS ?  <br>
A. Each docker service connects with another using embedded DNS instead of ip address

14. How to identify the issue of the container which is exited ? <br>
A. It can be done using
   - docker logs for logs info
   - docker inspect for exit info

15. How to watch the logs as soon as container starts ? <br>
A. It is possible if you run the docker in attached mode

16. When we run docker-compose using docker images, will container be in attached or detached mode ? <br>
A.  It will be in detached mode

17. In which case, docker attach is useful ? <br>
A.  It is useful when you want to see live logs or find reason for failure

18. What is the use of docker run -it <CONTAINER> bash ?
A.  It is useful when you dont want to install anything directly on server but u want to test inside container

19. How to dynamically set value for docker ? <br>
A.  It can be done using environment variables

20. What is docker compose ? whats the use of it ? <br>
A.  Linking the containers together or bringing all the containers in same network, we use docker compose. Using simple docker, we need to link them 

21. 

** . Docker Architecture ? <br>
** . Docker Execution Steps ? <br>
