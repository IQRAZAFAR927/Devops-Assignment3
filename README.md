# Devops Course 2024

This repository contains the work completed for the DevOps Course 2024 assignment, which includes:

Guide to Learning and Contribution
View Blog Summaries
Sample repo from the internet and applying DevOps tooling.Pick and choose (your existing) knowledge and expand it to guide.
A sample landing page with my CV.

 # Documentation:

 .[VIEW BLOG SUMMARIES](https://github.com/IQRAZAFAR927/Devops-Assignment3/blob/4fac9e179f4efe774523636fb33934005d3d162d/blog_summaries.md)

 
 .[VIEW LEARNING](https://github.com/IQRAZAFAR927/Devops-Assignment3/blob/4fac9e179f4efe774523636fb33934005d3d162d/Guide_to_Learning_and_Contribution.md)

 
 .[CV](https://github.com/IQRAZAFAR927/Devops-Assignment3/blob/4fac9e179f4efe774523636fb33934005d3d162d/index.html)


   # Quick Guide to DevOps Implementation for Deploying a MERN Application

  This repository demonstrates the use of DevOps practices for deploying a MERN application to a cloud environment. By integrating automation, version control, and continuous delivery pipelines, this workflow ensures that the MERN stack application is deployed seamlessly and consistently. Below is a breakdown of key practices and steps for setting up this workflow.
   # Key DevOps Practices Applied:

1-Automation with CI/CD Pipelines:

Continuous Integration (CI) and Continuous Deployment (CD) pipelines automate the build, test, and deployment processes.
Tools like GitHub Actions or GitLab CI are configured to automatically build and test the application whenever changes are pushed to the repository.
The CD pipeline ensures the application is automatically deployed to a cloud environment (e.g., AWS, Heroku, DigitalOcean) after successful tests.

2-Containerization with Docker:

Docker is used to containerize the MERN application, ensuring that the app runs consistently across different environments.
A Dockerfile defines the container environment for both the backend (Node/Express) and frontend (React), while docker-compose.yml manages multi-container setups for both services.

3-Version Control and Collaboration:

The application is managed using Git for version control, ensuring proper tracking of changes, collaborative workflows, and rollback capability.
A Git branching strategy (e.g., Git Flow) is followed to organize development, testing, and production branches.

4-Infrastructure as Code (IaC)::

Using Terraform or AWS CloudFormation, infrastructure is defined as code, enabling automatic provisioning of cloud resources such as virtual machines, databases, and networking components.
This allows for easy and consistent deployment of cloud infrastructure with minimal manual intervention.

# Step-by-Step Guide to Implementing the Workflow:
1. Set Up the Environment
Clone the repository and navigate to the project directory:
      git clone <repository-url>
      cd <repository-directory>
Install required dependencies for both the backend (Node.js/Express) and frontend (React):
      cd backend
      npm install
      cd ../frontend
      npm install
2. Containerize the Application Using Docker
Backend: Create a Dockerfile for the backend that installs Node.js, copies application files, installs dependencies, and exposes the appropriate port
  # Backend Dockerfile
       FROM node:16
       WORKDIR /app
       COPY ./backend/package*.json ./
       RUN npm install
       COPY ./backend ./
       EXPOSE 5000
       CMD ["npm", "start"]
  Frontend: Create a Dockerfile for the frontend React application, which installs dependencies and builds the production-ready app:
       # Frontend Dockerfile
          FROM node:16
          WORKDIR /app
          COPY ./frontend/package*.json ./
          RUN npm install
          COPY ./frontend ./
          RUN npm run build
          EXPOSE 3000
          CMD ["npm", "start"]
    Docker Compose: Define services for the frontend, backend, and MongoDB database in a docker-compose.yml file:
                version: '3'
        services:
          backend:
            build: ./backend
            ports:
              - "5000:5000"
            depends_on:
              - mongo
          frontend:
            build: ./frontend
            ports:
              - "3000:3000"
          mongo:
            image: mongo
            ports:
              - "27017:27017"
    Run the multi-container application with:
         docker-compose up
3. Set Up Continuous Integration and Deployment (CI/CD)
Configure GitHub Actions (or another CI/CD tool) to automatically run tests and deploy the application. Create a .github/workflows/ci.yml file for GitHub Actions:
      name: CI/CD Pipeline
on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2
        
      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '16'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Build backend
        run: cd backend && npm run build

      - name: Deploy to Heroku (or other cloud provider)
        run: |
          heroku login
          heroku git:remote -a <heroku-app-name>
          git push heroku main
This file defines the CI pipeline that installs dependencies, runs tests, and deploys the application to a cloud environment (e.g., Heroku, AWS)
4. Configure Infrastructure as Code (IaC)
Use Terraform to define the infrastructure resources such as EC2 instances, load balancers, and databases:
         resource "aws_instance" "mern_app" {
           ami           = "ami-12345678"
           instance_type = "t2.micro"
           key_name      = "your-key-pair"
           tags = {
             Name = "MERN Application Server"
           }
         }
 Deploy infrastructure using:
        terraform init
       terraform apply
5. Monitor and Manage the Application
Use monitoring tools like Prometheus, Grafana, or New Relic to track application performance and uptime.
Set up alerts to notify when certain thresholds (e.g., high latency or low disk space) are crossed.

# Conclusion
By applying DevOps principles, this workflow ensures that the MERN application is deployed in a consistent, automated, and reliable manner. Docker containers provide environment consistency, while CI/CD pipelines automate testing and deployment. Infrastructure as Code ensures the cloud infrastructure is reproducible and manageable, making the deployment process more efficient and scalable.


# Blog summaries 
 # Blog 1
 The Car Modification Web Application is a groundbreaking solution for the automotive customization industry, addressing inefficiencies and communication challenges in traditional workflows. It offers a centralized platform with modules for customer car design, workshop management, and inventory control. Key features include real-time visualization, 3D animations, and AI-driven recommendations to enhance user experience and streamline operations. The system benefits multiple stakeholders, including customers, modifiers, and suppliers, by providing intuitive tools and organized processes.  

Built using modern technologies like React, Node.js, and TensorFlow, the platform integrates seamlessly with 3D and VR libraries for immersive experiences. It ensures efficient inventory management, facilitates smooth collaboration between users, and provides robust administrative control through real-time analytics. By combining innovation with usability, this application aims to transform automotive customization into a faster, more engaging, and user-centric experience, setting new industry standards.
 
[Blog 1](https://medium.com/@i202401/revolutionizing-car-customization-introducing-the-car-modification-web-application-2a3e87594d65)


# Blog 2

The blog effectively guides readers through the process of pushing an application to a GitHub repository, making it especially valuable for beginners in software development. The instructions are detailed, covering everything from setting up a GitHub account to pushing code to a remote repository. The step-by-step approach, coupled with command-line examples, ensures that users can easily follow the process, even if they are unfamiliar with Git.

One of the key strengths of the blog is its clarity and accessibility, providing a simple yet comprehensive explanation of version control concepts. By using visual aids and breaking down each step into digestible chunks, the blog empowers users to confidently integrate Git into their workflow. Additionally, it emphasizes the importance of regularly committing and pushing changes, reinforcing best practices for code management.

[BLog2](https://medium.com/@i202401/how-to-push-your-application-to-a-github-repository-7190acaf38a1)


# CV

# Hi,'I am IQRA ZAFAR 
As a skilled UI/UX and product designer, I specialize in crafting intuitive and visually appealing user experiences that align with modern design principles. With expertise in user research, wireframing, prototyping, and interface design, I excel in delivering innovative and user-centered solutions that enhance functionality and drive business success.

# :round_pushpin: Connect With me 
# :e-mail:iqrazafar927@gmail.com
# linkdin:(linkedin.com/in/iqrazafar)

# Education 🎓
. BS Software Engineering 

 .Graduation 2025

 # 💡 Skills
Programming Languages: Java, Python, JavaScript, C++
UI/UX Designing: Figma, Photoshop, Behance
Natural Language Processing: Text Preprocessing, Sentiment Analysis, Language Models
Web Development: HTML, CSS, JavaScript, React, Node.js
Version Control: Git, GitHub
Project Management: Agile Methodologies

# 📁 Projects
# AutoMorphix: Mern website intregated with Unity
Description: Automorphix is a MERN-based website integrating Unity WebGL, allowing customers to visualize real-time car modifications, with dedicated modules for modifiers to validate changes and admins to manage users, modifiers, and customers

# HealthCare Application
Description: HealthCare is an application that manages doctors, nurses, and patients, featuring modules for disease prediction, AI Modal training, report generation, and appointment scheduling with doctors.

# Emotion Detection using NLP 
Emotion Detection in Crises is an NLP project that analyzes social media text to predict emotions like anger, happiness, hope, and sadness during crises, enabling targeted assistance to areas in greatest need.

# 💼 Experience
# Lab Demonstrator at FAST-NUCES Islamabad campus 
June 2023 - Jan 2024

Jan 2024 - July 2024

Dusring lab, assist the students to solve their queries, code problem and errors.
Worked on problem solving problem.

# Team Ambassadors at NASCON'22

Apr 2022 - Jun 2022

# Team UI/UX team at NASCON'22

Apr 2022 - Jun 2022











   
