# Jenkins Pipeline Guide

## Prerequisites

- Jenkins 2.0+
- Git plugin
- GitHub plugin
- Email extension plugin

## Jenkinsfile Structure

```groovy
pipeline {
    agent any
    
    stages {
        stage('Source Control') {
            steps {
                git 'https://github.com/NageliDharmaNaidu/jenkins-demo-project.git'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building...'
                // Build commands here
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                // Test commands here
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Deploy commands here
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline complete!'
        }
    }
}
```

## Setting up GitHub Webhook

1. Go to GitHub repo Settings
2. Click Webhooks → Add webhook
3. Payload URL: `http://jenkins-server:8080/github-webhook/`
4. Content type: `application/json`
5. Select: Send me everything
6. Save