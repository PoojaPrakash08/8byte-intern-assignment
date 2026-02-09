# Project Approach

The goal of this assignment was to deploy a simple Node.js application on AWS using modern DevOps practices such as containerization, Infrastructure as Code, and CI/CD automation.

## Technology Choices

- **Node.js (Express):**  
  Used to build a lightweight web application with minimal setup.

- **Docker:**  
  The application was containerized to ensure consistency across local and cloud environments. Docker helps avoid dependency issues and makes deployment easier.

- **Terraform:**  
  Terraform was used to provision AWS infrastructure in a declarative way. This ensures the setup is repeatable, version-controlled, and easy to modify.

- **AWS EC2:**  
  An EC2 instance was chosen to host the Dockerized application because it provides full control over the environment and is suitable for learning core DevOps concepts.

- **GitHub Actions:**  
  GitHub Actions was used to automate the Docker build process on every push to the main branch. This helps validate that the application can be built successfully.

## Infrastructure Design

The infrastructure includes:
- A custom VPC with a public subnet
- Internet Gateway and route table for internet access
- Security Group allowing SSH (22) and application access (3000)
- EC2 instance with Docker installed using user_data
- Elastic IP to ensure a stable public endpoint

## Deployment Strategy

The application is built into a Docker image and run as a container on the EC2 instance.  
Using Docker ensures that the same image can be built locally and in CI without changes.

Overall, this approach follows basic DevOps best practices while keeping the setup simple and understandable for a beginner.
