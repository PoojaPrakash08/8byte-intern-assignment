# 8byte Intern Assignment – CI/CD Deployment Project

## Project Overview

This project was done as part of the **8byte DevOps Intern Assignment**. The main goal of this project is to understand and implement a complete DevOps flow starting from application setup to deployment using cloud services and automation tools.

In this project, I have:

* Created an application and containerized it using Docker
* Provisioned AWS infrastructure using Terraform
* Deployed the application on an EC2 instance
* Implemented CI/CD using GitHub Actions
* Verified deployment through browser and pipeline execution

This project helped me understand real-world DevOps practices like Infrastructure as Code (IaC), containerization, and automated deployments.

---

## Architecture Overview

The architecture followed in this project is simple and easy to understand:

* Developer pushes code to GitHub repository
* GitHub Actions workflow is triggered automatically
* Application is built using Docker
* Terraform provisions AWS EC2 infrastructure
* Application is deployed on EC2 instance
* Application is accessed using EC2 public IP


---

## Steps to Run the Application Locally

1. Clone the repository:

```bash
git clone https://github.com/PoojaPrakash08/8byte-intern-assignment.git
cd 8byte-intern-assignment
```

2. Install required dependencies (Node.js / Python based on application).

3. Run the application locally:

```bash
npm install
npm start
```

4. Open browser and access:

```
http://localhost:3000
```

---

## Steps to Build Docker Image

1. Make sure Docker is installed and running.

2. Build Docker image using Dockerfile:

```bash
docker build -t 8byte-app .
```

3. Verify Docker image:

```bash
docker images
```

4. Run Docker container:

```bash
docker run -d -p 3000:3000 8byte-app
```

---

## Steps to Provision Infrastructure Using Terraform

1. Navigate to Terraform directory:

```bash
cd terraform
```

2. Initialize Terraform:

```bash
terraform init
```

3. Validate configuration:

```bash
terraform validate
```

4. Preview infrastructure changes:

```bash
terraform plan
```

5. Apply Terraform configuration:

```bash
terraform apply
```

6. After successful apply, EC2 instance will be created.

---

## Steps to Deploy Application on EC2

1. Connect to EC2 instance using SSH:

```bash
ssh -i key.pem ec2-user@<EC2_PUBLIC_IP>
```

2. Install Docker on EC2 instance.

3. Pull or build Docker image on EC2.

4. Run Docker container:

```bash
docker run -d -p 3000:3000 8byte-app
```

5. Access application in browser:

```
http://<EC2_PUBLIC_IP>
```

---

## GitHub Actions Workflow Explanation

GitHub Actions is used to automate the CI/CD pipeline. The workflow performs the following steps:

* Triggers on push to main branch
* Checks out the repository code
* Builds the Docker image
* Runs required checks
* Ensures successful build before deployment

This ensures that every code change is automatically tested and built without manual effort.

---

## Screenshots

The following screenshots are included in the repository:

* Terraform apply successful output
  <img width="966" height="521" alt="8byte_16" src="https://github.com/user-attachments/assets/8a49b32f-6d06-46a0-b520-5d40d15f0887" />
  <img width="751" height="395" alt="8byte_17" src="https://github.com/user-attachments/assets/1a7a6741-41a4-43fb-8cc8-41848849adca" />

* Running EC2 instance in AWS console
  <img width="1293" height="905" alt="8byte_18" src="https://github.com/user-attachments/assets/d4f287f7-e923-422c-b81d-8f45febc0fbe" />

* Application running in browser using EC2 public IP
  <img width="1287" height="243" alt="8byte_24" src="https://github.com/user-attachments/assets/8eb0ed90-c0b9-4753-88a2-d2d8ef82c1fb" />

* Successful GitHub Actions pipeline execution
  <img width="1918" height="875" alt="8byte_32" src="https://github.com/user-attachments/assets/fe5b27eb-2578-4864-a467-f36cb72df400" />


---

## Deliverables

* GitHub Repository:
  [https://github.com/PoojaPrakash08/8byte-intern-assignment](https://github.com/PoojaPrakash08/8byte-intern-assignment)

* Public Application URL:
  The application is deployed on an AWS EC2 instance and is accessible via the following Elastic IP when the instance    is running:
  http:](http://13.53.183.148:3000/)
  

* Screenshots folder containing:

  * Terraform output
  * EC2 instance status
  * Application UI
  * GitHub Actions pipeline

---

## Conclusion

This project gave me hands-on experience with DevOps tools like Docker, Terraform, AWS EC2, and GitHub Actions. It improved my understanding of CI/CD pipelines and cloud infrastructure deployment.
