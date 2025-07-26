## Demo Project - Complete CI/CD with Terraform

### Topics of the Demo Project
Complete CI/CD with Terraform

### Technologies Used
- Terraform
- Jenkins
- Docker
- AWS
- Git
- Java
- Maven
- Linux
- Docker Hub

### Project Description
Integrate provisioning stage into complete CI/CD Pipeline to automate provisioning server instead of deploying to an existing server
- Create SSH Key Pair
- Install Terraform inside Jenkins container
- Add Terraform configuration to application’s git repository
- Adjust Jenkinsfile to add “provision” step to the CI/CD pipeline that provisions EC2 instance
- So the complete CI/CD project we build has the following configuration:
  - a. CI step: Build artifact for Java Maven application
  - b. CI step: Build and push Docker image to Docker Hub
  - c. CD step: Automatically provision EC2 instance using TF
  - d. CD step: Deploy new application version on the provisioned EC2 instance with Docker Compose

                                   COMMAND                  CREATED          STATUS          PORTS                                       NAMES
# 459bc9f7af12   fsiegrist/fesi-repo:devops-bootcamp-java-maven-app-1.0.57-7   "/bin/sh -c 'java -j…"   53 seconds ago   Up 52 seconds   0.0.0.0:8000->8080/tcp, :::8000->8080/tcp   ec2-user-java-maven-app-1
```

Open the browser and navigate to 'http://3.76.7.164:8000' to see the java-maven-app in action.
