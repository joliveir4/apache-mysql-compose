# Apache-MySQL Docker Compose Project

This project sets up a web application environment using Docker Compose, featuring Apache HTTP Server and MySQL. It utilizes HTML, CSS, and JavaScript for the frontend, with Linux Bash scripts for Infrastructure as Code (IaC) to automate Docker installation and configuration. The deployment is designed for an AWS EC2 instance, leveraging Docker Swarm for orchestration and clustering.

## Features

- **Apache HTTP Server**: Serves the web application's frontend.
- **MySQL**: Provides the backend database service.
- **Docker Compose**: Manages multi-container Docker applications.
- **Docker Swarm**: Enables clustering and orchestration of Docker containers.
- **Infrastructure as Code (IaC)**: Automates setup using Bash scripts.

## Prerequisites

- AWS EC2 instance running a Linux-based operating system.
- [Docker](https://docs.docker.com/get-docker/) installed on the EC2 instance.
- [Docker Compose](https://docs.docker.com/compose/install/) installed on the EC2 instance.
- Basic knowledge of Docker and Docker Compose.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/joliveir4/apache-mysql-compose.git
   cd apache-mysql-compose

2. **Install Docker and Docker Compose**:
    - Execute the provided Bash script to install Docker and Docker Compose:
      ```bash
      ./provision.sh
      ```

3. **Deploy the Stack**:
    - Use Docker Compose to build and deploy the services:
      ```bash
      docker-compose up -d
      ```

4. **Initialize Docker Swarm** (Optional):
    - If you wish to use Docker Swarm for clustering and orchestration, initialize Swarm mode with this command:
      ```bash
      docker swarm init
      ```

5. **Access the Application**:
    - Once the services are running, you can access the web application via the EC2 instance's public IP address in your browser.
    - Example:
      ```plaintext
      http://<EC2_PUBLIC_IP>
      ```

---

That's it! You've successfully set up and deployed the Docker containers for Apache and MySQL on your AWS EC2 instance using Docker Compose.
