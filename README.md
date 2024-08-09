Name: Nicole Udochukwu

Project Title: Online Banking Application Deployment on Azure Cloud Platform.

Start Date: 2nd May 2024

End Date:21st July 2024

Role: Cloud Security Engineer


Description:

I spearheaded the development of a cutting-edge online banking application, leveraging a three-tier architecture to ensure PCI-DSS compliance. We carefully crafted a scalable and secure environment, integrating Azure Virtual Machines, Azure Network Security Groups, and Azure Virtual Network to provide a robust foundation. I oversaw the design and implementation of the frontend, utilizing Node.js, React.js, and JavaScript to deliver a seamless user experience. 

We developed a robust backend using Java, JDK 17, and Maven, and implemented a secure database management system using MySQL 8.0. Throughout the project, I ensured adherence to the highest security standards, utilizing SonarCloud for code analysis, conducting thorough code reviews, and performing regular security audits. By implementing multiple measures to protect user data and maintain the integrity of the application, we achieved a secure and compliant online banking solution.



Tools and Technologies Used

Git/Github: Utilized as a version control system to clone and manage the codebase for both the backend and frontend applications.

Draw.io: Employed to create a visual representation of the three-tier architecture, illustrating the interactions between the frontend, backend, and database components.

Confluence: Leveraged as a knowledge management platform to store, share, and collaborate on project documentation.

Jira: Used to plan, track, and manage the development and deployment of the online banking application, ensuring efficient project execution.

Slack: Facilitated team communication, enabling quick discussion, information sharing, and feedback exchange among team members.

Azure Entra ID: Provides identity and access management capabilities, ensuring secure authentication and authorization for users accessing the  servers.

Azure Policy: Enforces compliance with organizational policies and regulatory requirements, guaranteeing that deployments and configurations align with specified standards.

Azure Virtual Network: Establishes a secure and isolated network environment for the application, segregating it from the public internet.

Azure Network Security Group: Controls inbound and outbound network traffic, protecting servers from unauthorized access and threats by enforcing specified security rules and policies.

Azure Virtual Machine;  Provided a scalable and secure environment for hosting the application, allowing for the deployment of multiple virtual machines to support different workloads and applications.

Azure DNS Zone: Enabled the creation of DNS records, routing traffic to the application and allowing users to access it via a custom domain name.

Azure Public and Private IP: Assigned public and private IP addresses to each server (backend, frontend, and database), facilitating secure access and communication.

Port Configuration: Configured ports to enable communication between servers and applications, ensuring seamless data exchange.

Frontend Development Tools

Node.js: Served as the JavaScript runtime environment for building and running the frontend application.

React.js: Used as the JavaScript library for building reusable UI components and managing the application's state.

JavaScript: Used for client-side scripting and creating interactive web pages.

HTML: Used for structuring and organizing content on the web pages.

CSS: Used for styling and layout of the web pages.

NPM: Node Package Manager (NPM) was used to manage dependencies and install required packages for the project.

Backend Development Tools

Java: Used as the primary programming language for backend development.

JDK 17: Provided the Java Development Kit for compiling and running Java applications.

Maven: Managed dependencies and automated the build process for the Java-based backend application.

Database Management

MySQL 8.0: Used as the relational database management system for storing and managing data.

MySQL Workbench was utilized to test and verify the database's integrity and functionality following configuration adjustments.

Methodology

![Untitled Diagram drawio](https://github.com/user-attachments/assets/bcaf167f-f9b5-407a-880a-0acea2ad55fd)


A clear representation of a secure Online banking Application with compliance to PCI-DSS




Objective

Create a secure Online Banking Application compliant with PCI-DSS standards.

Infrastructure Setup

Resource Group Creation: Set up a resource group for organizing and managing related resources.

Virtual Network: Created a virtual network with three subnets for segregating traffic and enhancing security.

<img width="936" alt="Subnets Virtual Network" src="https://github.com/user-attachments/assets/fc29076c-1834-4691-b29a-0169d76b3787">

Network Security Groups: Configured three Network Security Groups (NSGs) for Database, Backend, and Frontend, each with specific rules to control traffic.

Virtual Machines: Provisioned three Ubuntu virtual machines for different tiers (database, backend, frontend) with data encrypted using SSL/TLS.

<img width="925" alt="Virtual machines" src="https://github.com/user-attachments/assets/ece612e2-6bde-4b66-8f29-5045bd0ccad2">

Database Creation and Server Configuration

1. NSG Configuration (Network Security Group)
   
Port 3306: Allowed access to the backend network block 

Port 22: Allowed access for configuration and management of the server

2. Server Access:
   
Used MobaXterm to access the server remotely using the public IP address and a private key for secure authentication via SSH.

3. MySQL Installation
   
Installed MySQL using a Bash script.

<img width="921" alt="bash" src="https://github.com/user-attachments/assets/8bdec53a-4c50-41ba-b7ce-b5ffae26fbc7">

Changed the default root password to a stronger one for security.

Completed the secure installation steps to prevent unauthorized access.

Created users with specific privileges to access the database.

4. Remote Connection Configuration
   
Configured the MySQL server to allow remote connections by setting the bind address parameter.

5. Validation and Testing
    
Tested and validated the setup using MySQL Workbench to ensure the database connection was working correctly.

<img width="933" alt="connected" src="https://github.com/user-attachments/assets/2dc0a84b-a66d-4bc8-aae3-823e004242db">

6. Security Measures
   
Later, to enhance security:
* Port 3306 was changed to a non-standard port to prevent unauthorized access.
* Port 22 was closed to prevent SSH access from external networks.
* The public IP address was deleted to prevent direct access to the server.
* The private IP address is now used for internal communication with the backend, ensuring the server is not accessible from external networks.




Backend Creation and Configuration

1. NSG Configuration (Network Security Group):
Port 8080: Allowed access to the Frontend Network block.
Port 22: Allowed access for configuration and management of the server.

2. Server Access
Used MobaXterm to access the server remotely using the public IP address and a private key for secure authentication via SSH.

3. Setup Steps
Updated the server to ensure it had the latest security patches and updates.

Installed JDK (Java Development Kit) 17, which is required for running the backend application.

Installed Maven, a build automation tool used to package and manage dependencies for the application.

Cloned the backend code from a GitHub repository, ensuring the latest version of the code is used.

Installed the MySQL Client to test and validate the connection to the MySQL Server Database.

Configured CORS (Cross-Origin Resource Sharing) security to restrict access to specific domains or IP addresses.

<img width="944" alt="DIGITALWITCH NGBACKEND" src="https://github.com/user-attachments/assets/dcc2c757-0371-4bf8-9d2c-4c8f647ab4b7">


4. Application Deployment : 
Packaged and ran the application using Maven, which compiled and executed the code.

![Screenshot 2024-08-04 060222](https://github.com/user-attachments/assets/3b52b06e-ff5c-4d90-a021-dd077d764a12)

6. Security Measures
   
Later, to enhance security:
* Port 22 was closed to prevent SSH access from external networks.
* The public IP address was deleted to prevent direct access to the server.
* The private IP address is now used for internal communication with the frontend, ensuring the server is not accessible from external networks.
* CORS security configuration ensures that only authorized domains or IP addresses can access the backend API, reducing the risk of unauthorized access.



Frontend Creation and Server Configuration


1.NSG Configuration (Network Security Group):

Port 3000: Allowed public access to the frontend server.

Port 22: Allowed access for configuration and management of the server via SSH (Secure Shell).

Port 443: Allowed public access for secure HTTP requests.

2.Server Access:
Used MobaXterm to access the server remotely using the public IP address and a private key for secure authentication via SSH.

3.Setup Steps:
Updated the server to ensure it had the latest security patches and updates.

Installed Node.js, a JavaScript runtime environment, which is required for the frontend application.

Installed npm (Node Package Manager), which is used to manage dependencies and install project-specific libraries.

Cloned the frontend code from a GitHub repository, ensuring the latest version of the code is used.

Configured the frontend to bind with the backend server on port 8080, allowing communication between the two services.

<img width="941" alt="frontend config backend" src="https://github.com/user-attachments/assets/c25bd0bd-542c-40b6-a7a1-f1565fea1586">

Installed project-specific dependencies using npm, ensuring all required libraries are available.

Installed React scripts, which provide additional features for the frontend application.

Started the development server, which provides a way to test and develop the application locally.

![Screenshot 2024-08-04 133540](https://github.com/user-attachments/assets/6787f832-c521-4283-9344-0d54459b2428)

4. Application Testing and Deployment:

Verified the application was functioning as expected.

Confirmed that the application was securely connecting to the backend server on port 8080.

<img width="954" alt="online banking frontend" src="https://github.com/user-attachments/assets/4aba8772-0f65-495c-8163-048791dedb34">


5. Security Measures
       
Later, to enhance security:

* Port 22 was closed to prevent SSH access from external networks, improving security by reducing potential vulnerabilities.


Security 

SonarCloud: Used to analyze code and identify potential security vulnerabilities.

Code Reviews: Conducted to ensure compliance with security best practices.

Regular Security Audits: Performed to identify and address potential security risks.



