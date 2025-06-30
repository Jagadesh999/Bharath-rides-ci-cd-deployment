#  Bharath Rides – DevOps CI/CD Project

Welcome to **Bharath Rides** – our own ride booking platform!  
This is a full real-time DevOps project where we took a simple frontend application (HTML/CSS/JS) and deployed it using a complete CI/CD pipeline on AWS.

>  “Bharath Ride is Ours. Let’s Engine!” – Powered by DevOps Automation 🔧

---

##  Project Objective

Automate the build, test, code quality check, and deployment of a simple web app using open-source DevOps tools.

-- 2. 💻 Minimum VM Requirements
Server	Tools Installed	OS	Fake IP (example)
VM1	Jenkins, Maven, Git, Docker	Ubuntu 20.04	54.101.22.33
VM2	Apache Tomcat	Ubuntu 20.04	3.110.45.89
VM3	SonarQube	Ubuntu 20.04	15.206.77.22

Use AWS EC2 t2.medium or t2.small based on budget.

## 🛠️ Tech Stack Used

| Area             | Tools Used                           |
|------------------|--------------------------------------|
| Source Control   | Git & GitHub                         |
| Build Tool       | Maven (for WAR packaging)            |
| CI/CD            | Jenkins                              |
| Code Quality     | SonarQube                            |
| Deployment       | Apache Tomcat (on AWS EC2)           |
| Scripting        | Bash, curl                           |
| Language         | HTML/CSS/JavaScript                  |

---

## 🗂️ Project Structure

bharath-rides-ci-cd-deployment/
├── application/ # Static Web App
│ └── index.html
├── pom.xml # WAR packaging config
├── Jenkinsfile # CI/CD Pipeline
├── sonar-project.properties # SonarQube config
├── screenshots/ # Optional UI/Pipeline Images
└── README.md # This file

pgsql
Copy
Edit

---

##  Jenkins Pipeline Overview

1. **Checkout** – Pull source code from GitHub  
2. **Build** – Run `mvn clean package` to generate `bharathrides.war`  
3. **Code Quality** – Analyze code using SonarQube  
4. **Deploy to Tomcat** – Upload WAR file via `curl` to Tomcat server on AWS EC2  

```groovy
curl -T target/bharathrides.war \
  http://admin:admin@<tomcat-ec2-ip>:8080/manager/text/deploy?path=/bharathrides&update=true
 Final Output
Access our deployed app here:

📍 http://3.110.45.89:8080/bharathrides


Jenkins pipeline success

App UI

SonarQube analysis

💡 What I Learned
WAR packaging even for frontend-only apps

Full Jenkins pipeline with SonarQube integration

Deployment to Apache Tomcat on EC2

CI/CD best practices: automation, standard naming, credentials usage

Real-time DevOps project lifecycle

👤 About Me
Busireddy Jagadeswar Reddy
DevOps Engineer | AWS Cloud | CI/CD Enthusiast
📧 jagadeeswarbusireddy@gmail.com
📱 +91 9182600992
🌐 GitHub – jagadesh999

🙌 Let's Connect
“Great DevOps isn’t just automation — it’s making your ride smoother.
Bharath Rides is ours. Let’s engine!”

![image](https://github.com/user-attachments/assets/91ae0341-a6bb-4fd0-a5dd-44ee2ef350c0)



