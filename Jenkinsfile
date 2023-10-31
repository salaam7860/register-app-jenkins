// Git Password ^^^^^^
/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    stages {
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout From SCM') {
            steps {
                /* groovylint-disable-next-line LineLength */
                git branch: 'main', credentialsId: 'Git_ID', url: 'https://github.com/salaam7860/register-app-jenkins.git'
         }
        }
        stage('Build Application') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
