📦 Jenkins CI/CD Pipeline Deployment on AWS
This project demonstrates the complete setup of a Jenkins CI/CD pipeline on AWS, integrated with GitHub and Apache Tomcat, to automate the build and deployment of a sample Java web application (swiggy.war).

🚀 Key Components
Jenkins Installation on EC2

Amazon Linux 2 (t2.micro)

Jenkins installed via shell script

Ports 22 (SSH) and 8080 (Jenkins UI) exposed

Apache Tomcat on EC2

Tomcat 9 deployed on a second EC2 instance

Custom user roles and security configured

Application deployment endpoint enabled

CI/CD Workflow

GitHub Integration (pull Java code)

Maven build (clean package)

WAR file deployment to remote Tomcat via Jenkins "Deploy to container" plugin

Tools & Technologies

AWS EC2

Jenkins

Apache Tomcat

Maven

Git

Bash Scripts

📂 Repository Structure
bash
Copy
Edit
├── jenkins.sh      # Jenkins installation and setup script
├── tomcat.sh       # Tomcat setup script with manager access
├── README.md       # Project description and instructions
🔧 How to Use
Deploy Jenkins: Use jenkins.sh to install and start Jenkins on EC2.

Setup Tomcat: Launch another EC2 instance and run tomcat.sh.

Create Jenkins Job:

Use GitHub repo as source

Build using Maven

Post-build action: deploy WAR to Tomcat

🌐 Access URLs
Jenkins: http://<jenkins-public-ip>:8080

Tomcat: http://<tomcat-public-ip>:8080

App URL: http://<tomcat-public-ip>:8080/swiggy
