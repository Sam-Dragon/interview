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

10. Docker Client Vs Docker Deamon Vs Docker Engine.?
- Docker client or docker cli is responsible for accepting all the commands from user and send it to appropritate api
- Docker Deamon is backend thread which is responsible for executing those commands and return the results
- Docker Engine = Docker CLI + API's + Docker Deamon

11. What are C-groups in docker ?
A. To control the amount of hardward / cpu to allocate for docker [option: --cpu or --memory]

12. What are docker network types ? which is default.
A.  bridge [default], none, host

13. What is embedded DNS ?
A. Each docker service connects with another using embedded DNS instead of ip address
