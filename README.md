# 🚀 Image to PDF Converter (AWS + Docker + ECS)

## 📌 Project Overview

This project is a web application that converts images into PDF format.
The application is containerized using Docker and deployed on AWS using ECS (Fargate) with ECR and Application Load Balancer.

---

## 🛠️ Tech Stack

* Frontend: React (Vite)
* Containerization: Docker
* Cloud: AWS (ECR, ECS Fargate, ALB)
* Deployment: ECS Service

---

## 🧱 Architecture

<img width="659" height="593" alt="image" src="https://github.com/user-attachments/assets/ac79bc34-61ad-4247-a02b-8f1897060d27" />

---

## ⚙️ Step-by-Step Process

### 1. Build Application

* Created frontend using React (Vite)
* Implemented image to PDF conversion logic

### 2. Dockerization

* Created Dockerfile
* Built Docker image:

```bash
docker build -t img-to-pdf .
```

### 3. Run Locally

```bash
docker run -p 3000:80 img-to-pdf
```

### 4. Push to AWS ECR

* Created ECR repository
* Tagged image

```bash
docker tag img-to-pdf:latest <ECR_URI>
```

* Pushed image:

```bash
docker push <ECR_URI>
```

### 5. ECS Deployment

* Created Task Definition
* Added container using ECR image
* Configured CPU & Memory

### 6. Create ECS Service

* Used Fargate
* Enabled Load Balancer
* Set port 80

### 7. Load Balancer Setup

* Created Application Load Balancer
* Configured Target Group
* Enabled public access

### 8. Final Deployment

* Application accessible via Load Balancer URL

---

## 🌐 Live Demo

Access the application using:
http://web-app-lb-929074018.eu-north-1.elb.amazonaws.com/

---

## 📌 Key Features

* Upload images
* Convert to PDF
* Fast processing
* Cloud deployment

---

## 📷 Screenshots

<img width="1577" height="799" alt="image" src="https://github.com/user-attachments/assets/257e5b85-230a-4c46-993c-8bddd2be53e1" />

---

## 💡 Future Improvements

* Add backend API (Node.js)
* Store files in S3
* Add authentication

---

## 👩‍💻 Author

Subashini
