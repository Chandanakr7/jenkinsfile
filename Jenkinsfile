pipeline {
    agent any
    
    tools {
        maven 'maven' // Ensure 'maven' is the correct name of the Maven tool in your Jenkins configuration
    }
    
    stages {
        stage('pull') {
            steps {
                  git branch: 'main', url: 'https://github.com/Chandanakr7/jenkinesss.git', credentialsId: 'your-credentials-id'
            }
        }
        
        stage('clean') {
            steps {
                sh 'mvn clean'
            }
        }
        
        stage('validate') {  // Corrected the typo
            steps {
                sh 'mvn validate'
            }
        }
        
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
