pipeline {
    agent any  // Defines the environment where the pipeline runs

    stages {

stage('clone') {  // Stage for building your project
            steps {
                // echo 'Building the project...'
                git 'https://github.com/gollapallydeepthi/devops__.git'
                // Add build commands here (e.g., mvn, npm, etc.)
            }
        }
               
stage('Build') {  // Stage for building your project
            steps {
                echo 'Building the project...'
                sh 'javac Helloworld.java'
                // Add build commands here (e.g., mvn, npm, etc.)
            }
        }
       
        stage('Test') {  // Stage for testing the project
            steps {
                echo 'Running tests...'
            sh  'java Helloworld'
                // Add test commands here (e.g., mvn test, npm test, etc.)
            }
        }
       
        stage('Deploy') {  // Stage for deploying your project
            steps {
                echo 'Deploying the project...'
                // Add deployment commands here
            }
        }
    }
   
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
