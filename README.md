

# 🚀 MEAN Stack DevOps CI/CD Project

This project demonstrates a  production-ready full-stack MEAN application  using the MEAN stack (MongoDB, Express, Angular 15, and Node.js). The backend will be developed with Node.js and Express to provide REST APIs, connecting to a MongoDB database. The frontend will be an Angular application utilizing HTTPClient for communication. 

The application will manage a collection of tutorials, where each tutorial includes an ID, title, description, and published status. Users will be able to create, retrieve, update, and delete tutorials. Additionally, a search box will allow users to find tutorials by title.

---

## Architecture Overview

**Tech Stack & Tools**

- Frontend: Angular 15  
- Backend: Node.js + Express (REST APIs)  
- Database: MongoDB  
- Reverse Proxy: Nginx  
- CI/CD: GitHub Actions  
- Containerization: Docker & Docker Compose  
- Container Registry: Docker Hub  
- Cloud Platform: AWS EC2 (Ubuntu)

Architecture Diagram:  
Architecture-diagram.png

---

##  CI/CD Workflow

1. Developer pushes code to GitHub  
2. GitHub Actions workflow is triggered  
3. Docker images are built for frontend & backend  
4. Images are pushed to Docker Hub  
5. AWS EC2 pulls the latest images  
6. Docker Compose restarts containers automatically  

---

## Dockerized Services

- Angular Frontend Container  
- Node.js Backend Container  
- MongoDB Container  
- Nginx Reverse Proxy (Port 80)  

---

## Application Flow

User / Browser  
→ Nginx (Reverse Proxy)  
→ Angular Frontend  
→ Node.js Backend  
→ MongoDB  

---

## Production Deployment (AWS EC2)

### Prerequisites
- AWS EC2 (Ubuntu)
- Docker installed
- Docker Compose installed
- Docker Hub account

### Run Application on EC2
```bash
docker compose pull
docker compose up -d
```

Application URL:
`http://<EC2-PUBLIC-IP>`


---

##  Local Development Setup      

### Node.js Server (Backend)
cd backend
npm install
RUN `node server.js`

You can update the MongoDB credentials by modifying the 
MongoDB config: `app/config/db.config.js`



### Angular Client (Frontend)
cd frontend
npm install
RUN `ng serve --port 8081`

You can modify the `src/app/services/tutorial.service.ts` file to adjust how the frontend interacts with the backend.

Local URL:
`http://localhost:8081`

---

## Features

- CRUD operations on tutorials  
- Search tutorials by title  
- RESTful APIs  
- Containerized services  
- Automated CI/CD pipeline  
- Nginx reverse proxy  

---

