# QR Code Generator - Dockerized Application

This project demonstrates how to dockerize a Python application that generates QR codes from a given URL. The application is containerized using Docker and automated using GitHub Actions for continuous integration.

## Initial steps:

1. Check Docker version:
```bash
docker --version
```
2. Dockerizing the QR Code Generator
```bash
pip freeze > requirements.txt
```
Git Steps:
1. Initilaize Git repository:
```bash
git init
```
2. Making initial commit:
```bash
git add .
git commit -m "Initial commit of QR Code Generator application"
```
3. Push repository to Github:
```bash
git remote add origin https://github.com/your-username/qr-code-generator.git
git push -u origin main
```

## How to Run

### Using Docker

1. Build the Docker image:

```bash
docker build -t qr-code-generator-app .
```

2. Running the Docker Container(detached mode): 
```bash

docker run -d --name qr-generator qr-code-generator-app
```
3. Checking Container Logs
```bash
docker logs qr-generator
```
4. Running with Custom URL
```bash
docker run -d --name qr-generator qr-code-generator-app --url http://www.njit.edu
```
5. Mounting Local Directory for QR Codes
```bash 
docker run -v ./qr_codes:/app/qr_codes qr-code-generator-app --url http://www.njit.edu
```
6. Stopping and Removing Container
```bash
docker stop qr-generator
docker rm qr-generator
```
7. Login to Docker:
```bash
docker login
```
8. Tag Docker image:
```bash
docker tag qr-code-generator-app your-dockerhub-username/qr-code-generator-app
```