# customer-service
Note :  If we want to run the application against a local database, set `Server=localhost;Database=ecomcustomerdb;User=root;Password=<password>;Port=3306;` in `appsettings.json`

# docker
When two developers are working on an application, one developer might have a different version of certain dependencies, such as MySQL, .NET SDK, and other components. If they configure the application based on the versions available on their machine, another developer with different versions may face compatibility issues. To run the application, the second developer must install the specific versions used by the first developer, which is time-consuming.
In the future, if a new team member joins and has the latest versions of these dependencies installed, they will also need to install older versions to match the application's requirements. This can be frustrating because it requires manual configuration.
Docker solves this problem by making applications portable. Instead of each developer manually configuring their environment, Docker ensures that the application runs in a consistent environment across different machines. This means the same versions of dependencies are used regardless of the developer's local setup, making it easier to share and deploy the application across multiple environments.

Commonly used commands:
 1. List all available containers : docker ps -a
 2. List running containers : docker ps
 3. Pull an image from Docker Hub : docker pull <image_name>:<tag>
 4. Build an image from a Dockerfile : docker build -t <image_name> .
 5. Start a stopped container : docker start <container_id_or_name>
 6. Stop a running container : docker stop <container_id_or_name>
 7. Get logs of a container : docker logs <container_id_or_name>
 8. Run a container from an image, automatically create and start it: docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>
 9. Remove stopped container : docker rm <container_id_or_name>
 10. Remove an image : docker rmi <image_name>
 11. Remove all containers : docker containers prune
 12. Run MySQL inside a container: docker exec -it <container_name> mysql -u<root> -p<password>






