# Docker Website Hosting Project

A simple and attractive website hosted inside a Docker container using Nginx.

## Project Overview

This project demonstrates how Docker can be used to containerize and deploy a static website. The website was built using HTML and CSS and then hosted inside an Nginx container.

The objective of this project was to understand Docker fundamentals, containerization, image creation, port mapping, and website deployment.

---

## Architecture

User Browser
↓
VM Public IP:8080
↓
Docker Container
↓
Nginx Web Server
↓
HTML + CSS Website

---

## Technologies Used

- Docker
- Nginx
- HTML5
- CSS3
- Git
- GitHub
- Ubuntu Linux

---

## Project Files

```text
docker-website-project/
│
├── Dockerfile
├── index.html
├── README.md
└── .gitignore
```

---

## What is Docker?

Docker is a containerization platform that packages an application along with its dependencies into lightweight and portable containers.

Benefits:

- Lightweight
- Fast deployment
- Portable
- Isolated environment
- Easy to scale

---

## What is a Container?

A container is an isolated environment where an application runs independently without affecting the host operating system.

In this project:

- Nginx runs inside the container.
- The website files are served by Nginx.
- Users access the website through the VM's public IP.

---

## How This Project Works

### Step 1: Create Website

Create an HTML and CSS based website.

### Step 2: Create Dockerfile

Use Nginx as the base image and copy the website into the Nginx directory.

### Step 3: Build Docker Image

Create a Docker image from the Dockerfile.

### Step 4: Run Docker Container

Launch a container and expose it to the outside world using port mapping.

### Step 5: Access the Website

Open the website in a browser using:

```text
http://<VM_PUBLIC_IP>:8080
```

---

## Docker Commands Used

### Build Image

```bash
docker build -t mywebsite .
```

### Run Container

```bash
docker run -d --name website-container -p 8080:80 mywebsite
```

### Check Running Containers

```bash
docker ps
```

### View Logs

```bash
docker logs website-container
```

### Stop Container

```bash
docker stop website-container
```

### Start Container

```bash
docker start website-container
```

### Remove Container

```bash
docker rm -f website-container
```

---

## Port Mapping

```text
VM Port 8080 ---> Container Port 80
```

When a user opens:

```text
http://<VM_PUBLIC_IP>:8080
```

The request is forwarded to the Nginx web server running inside the Docker container.

---

## Firewall Configuration

### VM Firewall

```bash
ufw allow 8080/tcp
```

### Cloud/VCD Firewall Rule

Allow:

- Protocol: TCP
- Port: 8080

---

## Learning Outcomes

Through this project, I learned:

- Docker fundamentals
- Containerization concepts
- Docker image creation
- Dockerfile usage
- Nginx deployment
- Port mapping
- Linux commands
- Git and GitHub integration
- Website deployment inside containers

---

## Future Improvements

- Add Docker Compose
- Add custom domain support
- Add SSL (HTTPS)
- Deploy multiple containers
- Integrate CI/CD pipeline
- Deploy on cloud infrastructure

---

## Author

Chand Perveen

B.Tech Computer Science Engineering

Interested in:

- Cybersecurity
- Cloud Computing
- DevOps
- Infrastructure Monitoring
