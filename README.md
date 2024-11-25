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


   # Quick Guide to DevOps Implementation in the Data Preprocessing Workflow

   This repository applies DevOps principles to automate and streamline a data preprocessing workflow for scraping and processing BBC News website data. Here's a breakdown of how DevOps is utilized and a guide to implementing it:
   # Key DevOps Practices Applied:

1-Automation with Apache Airflow:

An Airflow DAG (bbc_news_dag) automates the daily execution of data extraction and preprocessing tasks, reducing manual intervention and ensuring consistency.

2-Version Control with DVC:

Data Version Control (DVC) tracks versions of the preprocessed data stored in CSV files. This ensures reproducibility, collaboration, and rollback capabilities.

3-Code and Workflow Management:

A structured Python script (fetch_and_preprocess_data.py) performs extraction and preprocessing using libraries like BeautifulSoup and requests.
The GitHub repository maintains documentation and code organization, following DevOps best practices for codebase management.

4-Infrastructure as Code (IaC):

The use of Docker simplifies setting up and running Apache Airflow, encapsulating dependencies and ensuring a consistent environment.

# Step-by-Step Guide to Implementing the Workflow:
"Setting up Environmnet

. Install Python and ensure pip is available.

Clone the repository:

git clone <repository-url>
cd <repository-directory>

.Install required dependencies:
pip install -r requirements.txt

.Run the python script
python fetch_and_preprocess_data.py

.intialzie DVC
dvc init
dvc add preprocessed_data.csv

.Track changes 
git add preprocessed_data.csv.dvc .gitignore
git commit -m "Add preprocessed data with DVC"
dvc push

.automate with apache workflow
docker-compose up


# Conclusion
This workflow demonstrates the effective application of DevOps practices, combining automation, version control, and reproducibility. By integrating Airflow and DVC, the pipeline ensures consistent and scalable data preprocessing.


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











   
