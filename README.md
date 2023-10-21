YOLO Application
Overview
The YOLO application is a simple web application that consists of a client and a backend service. The client is a front-end application responsible for user interface and interactions, while the backend service provides necessary functionality to the client. This application uses Docker containers for easy deployment and management.

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
Vagrant: Ensure Vagrant is installed on your local machine.
VirtualBox: Install VirtualBox for running the Ubuntu virtual machine.
Ansible: Make sure Ansible is installed on your local machine.
How to Run the Application
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd yolo-app
Edit Hosts File:

Open the hosts file and replace <server-ip> with the IP address of your server.
Provision the Virtual Machine:

Run the following command to set up the virtual machine and install necessary packages using Vagrant and Ansible:
bash
Copy code
vagrant up --provision
Access the Application:

Once the provisioning is successful, access the application in your browser using the server IP address:
Client: http://<server-ip>:3000
Backend: http://<server-ip>:5000
Stopping the Application:

To stop the application and the virtual machine, run:
bash
Copy code
vagrant halt
Additional Notes
Ensure the necessary ports (3000 and 5000) are open on your server.
You can customize the application by editing the docker-compose.yml file and the corresponding Ansible playbook and roles.
