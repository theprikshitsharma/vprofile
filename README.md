# Automated 3-Tier Application Stack Setup  

This project demonstrates the automated provisioning of a 3-Tier Application Stack using Vagrant and provisioning scripts. The stack includes **MySQL/MariaDB, Memcached, RabbitMQ, Tomcat, and Nginx**, with the setup handled entirely through automation.

## Automation Workflow  
1. **Vagrant Configuration**:  
   - The `Vagrantfile` is configured to provision virtual machines (VMs) and execute specific provisioning scripts for each VM.  

2. **Provisioning Scripts**:  
   - Each VM runs its own provisioning script automatically during setup.  
   - These scripts handle the installation and configuration of services such as MySQL/MariaDB, Memcached, RabbitMQ, Tomcat, and Nginx.  

3. **Automated Setup**:  
   - Simply run `vagrant up` to start the provisioning process.  
   - VMs are brought up one by one, executing their respective provisioning scripts.  
   - Note: The process may take time. If it fails midway, running `vagrant up` again will continue the setup.  

4. **Validation**:  
   - Once all VMs are provisioned, the stack is verified by accessing the application through a web browser.  

## Key Highlights  
- **Hands-Free Deployment**: Eliminates the need for manual login and configuration.  
- **Repeatable Process**: The setup can be recreated effortlessly on any system with Vagrant installed.  
- **Integrated Services**: The application stack is configured to handle requests seamlessly across all tiers.  

### End-to-End Workflow  
1. The **Nginx** load balancer routes requests to the **Tomcat** server.  
2. The **Tomcat** server interacts with:  
   - **RabbitMQ** for message brokering  
   - **Memcached** for caching  
   - **MySQL/MariaDB** for database operations  
3. Cached results in **Memcached** reduce database load and optimize performance.  

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
# Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql


