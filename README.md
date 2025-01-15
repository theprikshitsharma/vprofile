# Manual 3-Tier Application Stack Project  

![image](https://github.com/user-attachments/assets/679d2eb2-31ce-47a8-87e2-1d6f012bbbf4)

In this project, I manually provisioned virtual machines using a Vagrantfile to establish a 3-Tier Application Stack consisting of **MySQL/MariaDB, Memcached, RabbitMQ, Tomcat, and Nginx**. Linux server configurations were meticulously handled using a Bash script.  

## Project Workflow  
- **Virtual Machine Provisioning**: Leveraged Vagrant with Oracle VirtualBox to create and manage virtual machines.  
- **Manual Configuration**: Logged into each virtual machine individually and executed shell commands via Bash to configure the required services.  
-  **Service Deployment**: Set up and integrated services, including:  
  - MySQL/MariaDB for database management  
  - Memcached for caching  
  - RabbitMQ as a message broker  
  - Tomcat for the Java application server  
  - Nginx as a load balancer  
-  **Artifact Deployment**: Compiled the application using Maven and deployed the generated artifact to the Tomcat server.  
-  **System Validation**: Conducted end-to-end testing by accessing the application via a web browser to ensure functionality and service integration.  

## Process Overview 

![image](https://github.com/user-attachments/assets/66b4b5e0-7012-4016-8a65-0229c214252a)

1. Requests from the **Nginx** load balancer were routed to the **Tomcat** server.  
2. The **Tomcat** server processed the requests, interacting with:  
   - **RabbitMQ** (message broker)  
   - **Memcached** (caching layer)  
   - **MySQL/MariaDB** (database layer)  
3. The application logic executed on the **Tomcat** server cached frequently accessed data in **Memcached**, reducing database load and improving performance.  

# Prerequisites
#
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL


