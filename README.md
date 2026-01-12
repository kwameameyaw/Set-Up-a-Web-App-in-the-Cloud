<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Set Up a Web App in the Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-vscode)

**Author:** Kwame Ameyaw  
**Email:** kwameameyaw@aol.com

---

## Set Up a Web App Using AWS and VS Code

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_7a1de541)

---

## Introducing Today's Project!

In this project, I will set up a web app in the Cloud. I'm doing this project to learn how to build a web app using AWS and VS Code.

This project is part one of a series of DevOps projects where I'm building a CI/CD pipeline! I'll be working on the next project tomorrow. 

I did this project today to expand my knowledge on how web apps are hosted on servers.

### Key tools and concepts

Services I used were EC2 and IAM. Key concepts I learnt include connecting to an EC2 via SSH,  connecting to an EC2 through IDE (VS Code), and creating a web app on the EC2.

### Project reflection

This project took me approximately 2 hours. The most challenging part was getting the ssh -i command syntax right. 

One thing I didn't expect in this project was having to use the Remote -ssh extension to connect to the EC2. 

---

## Launching an EC2 instance

### What I did in this step

In this step, I will launch an EC2 instance, as we'll use a virtual server to host our development work.

I started this project by launching an EC2 instance, as it will provide the necessary compute resources for deploying the application.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_7852fbf3)

### I also enabled SSH

SSH is a secure protocol used to remotely access and manage servers over an encrypted connection. I enabled SSH so that I can securely connect to the EC2 instance from my local machine to install software.

### Key pairs

A key pair is a set of cryptographic keys used to securely authenticate access to a server.

### Downloaded key pair file

Once I set up my key pair, AWS automatically downloaded the private key to my computer.

---

## Set up VS Code

### What I did in this step

In this step, I will connect to my EC2 instance via SSH because I need secure, direct access to the server to configure it, install software, and verify that my cloud environment is set up correctly.

### What is VS Code?

VS Code is a code editor developed by Microsoft that allows developers and engineers to write code, manage files, and work with terminals all in one place.

I will use VS Code to connect to my EC2 instance via SSH, run terminal commands, edit configuration and application files, and manage my project code in one centralized workspace.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_53d05e68)

---

## My first terminal commands

A terminal is where you send instructions to your computer using text instead of clicks. The first command I ran for this project is cd ~/Desktop/Devops

### Updating file permissions

I also updated my private key's permissions by running chmod 400 ./nextwork-keypair.pem to make the private key read-only.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_9328ada1)

---

## SSH connection to EC2 instance

### What I did in this step

In this step, I will connect to my EC2 via SSH.

### Connecting to EC2

To connect to my EC2 instance, I ran the command ssh -i ~/Desktop/DevOps/nextwork-keypair.pem ec2-user@ec2-3-21-93-56.us-east-2.compute.amazonaws.com

### This command required an IPv4 address

A server’s IPv4 DNS is the public domain name that resolves to the server’s IPv4 address, allowing anyone with permission to access the server over the internet without needing to remember its numeric IP address.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_e3069dca)

---

## Maven & Java

### What I did in this step

In this step, I will install Apache Maven on your EC2 instance, install Amazon Corretto 8, and verify the installations.



### Why I'm using Maven

Apache Maven is a build automation and project management tool primarily used for Java projects.

Maven is required in this project because it automates building, testing, and managing dependencies for my Java application, ensuring that all required libraries are correctly downloaded and configured, and that the application can be reliably compiled and deployed on the EC2 instance without manual setup.

### Why I'm using Java

Java is a popular programming language used to build different types of applications, from mobile apps to large enterprise systems.

Java is required for this project because Maven relies on Java to operate. So if we don't install Java, we won't be able to use Maven to generate/build our web app today.

---

## Create the Application

### What I did in this step

In this step, I will run Maven commands in my terminal to generate a Java web app.

### Creating the Java web app

I generated a Java web app using the command mvn archetype:generate \
   -DgroupId=com.nextwork.app \
   -DartifactId=nextwork-web-project \
   -DarchetypeArtifactId=maven-archetype-webapp \
   -DinteractiveMode=false


### Installing Remote - SSH

I installed Remote - SSH, which is an extension in VS Code lets you connect directly via SSH to another computer securely over the internet. I installed it to use VS Code to work on files or run programs on that server, just as I would on my own computer, which will come in handy when we edit the web app in your EC2 instance.

### SSH configuration details

Configuration details required to set up a remote connection include host, identityfile, and user.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_2939cf01)

---

## Create the Application

### Exploring the project structure

Using VS Code's file explorer, I could see the nextwork-web-project folder, which contains the source code for the webapp and the Maven Project Object Model file, which stores information and configuration details that Maven will use to build the project.

Two of the project folders created by Maven are src and webapp, which hold all the source code files that define how your web app looks and works.

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_45f91fd7)

---

## Using Remote - SSH

### What I did in this step

In this step, I will set up a connection between VS Code and my EC2 instance.

### Updating the web app

The index.jsp is a file used in Java web apps. It's similar to an HTML file because it contains markup to display web pages.

I edited index.jsp by changing the placeholder code to the code snippet below:
<html>

<body>

<h2>Hello !</h2>

<p>This is my NextWork web application working!</p>

</body>

</html>

![Image](http://learn.nextwork.org/amused_green_smart_grape/uploads/aws-devops-vscode_7a1de541)

---

## Using nano

### Additional improvements

### Terminal vs IDE

### Verifying my work

---

---
