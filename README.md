YOLO Application

Overview

This YOLO application is a simple web application that consists of a client and a backend service. The client is a front-end application responsible for user interface and interactions, while the backend service provides necessary functionality to the client. This application uses Docker containers for easy deployment and management.

Elements of the Application
1. Client:
The client component is responsible for the user interface.
It runs on port 3000.
2. Backend:
The backend component provides necessary API services to the client.
It runs on port 5000.
3. Docker:
Docker is used for containerization of both client and backend services.
Docker Compose is utilized for managing multi-container Docker applications.
4. Ansible:
Ansible is used for automated provisioning and deployment of the application.
Ansible roles are organized to handle different aspects of the deployment process.

Prerequisites
-Vagrant: Ensure Vagrant is installed on your local machine.
-VirtualBox: Install VirtualBox for running the Ubuntu virtual machine.
-Ansible: Make sure Ansible is installed on your local machine.

How to Run the Application
Clone the Repository:

-git clone <repository-url>
-cd yoloapp

Edit Hosts File:

Open the hosts file and replace <server-ip> with the IP address of your server.
Provision the Virtual Machine:

Run the following command to set up the virtual machine and install necessary packages using Vagrant and Ansible:

-vagrant up --provision

Access the Application:

-vagrant ssh : To go to the server
-cd /yolo :To go to the application directory where the docker-compose file is
-sudo docker-compose up -d :To start the 2 containers
-sudo docker ps: To see if the containers are running

Once this is successful, access the application in your browser using the server IP address:
-http://localhost:3000 since we forwarded the server ports to the host


Stopping the Application:
To stop the application and the virtual machine, run:

-vagrant halt

Additional Notes
Ensure the necessary ports (3000 and 5000) are open on your server.
You can customize the application by editing the docker-compose.yml file and the corresponding Ansible playbook and roles.