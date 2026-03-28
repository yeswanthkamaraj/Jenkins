## 🎯 Objectives
- Automate build and deployment process  
- Integrate version control (GitHub) with Jenkins  
- Reduce manual errors in deployment  
- Enable faster and reliable delivery  

---

## 🛠️ Tech Stack
- Jenkins  
- Java (Sample Project)  
- Git & GitHub  
- Maven / Gradle  
- Docker (Optional)  
- Kubernetes (Optional)  

---

## ⚙️ Jenkins Setup

### 1. Install Jenkins
```bash
java -jar jenkins.war
2. Access Jenkins
http://localhost:8080
3. Unlock Jenkins

Use the initial admin password:

~/.jenkins/secrets/initialAdminPassword
🔗 GitHub Integration
Go to Manage Jenkins → Plugins
Install:
Git Plugin
GitHub Plugin
Configure Git credentials
🏗️ Pipeline Configuration
🔹 Freestyle Job Steps
Source Code Management → Add Git Repository URL
Build Step → Execute Shell / Windows Batch
javac Main.java
java Main
🔹 Jenkins Pipeline (Jenkinsfile)
pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'javac Main.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Main'
            }
        }
    }
}
🔄 CI/CD Workflow
Developer pushes code to GitHub
Jenkins detects changes (Webhook / Poll SCM)
Build is triggered automatically
Code is compiled & tested
Deployment happens (optional)
📦 Key Features
✅ Automated Build Process
✅ Continuous Integration
✅ Pipeline as Code (Jenkinsfile)
✅ Easy GitHub Integration
✅ Scalable CI/CD Workflow
