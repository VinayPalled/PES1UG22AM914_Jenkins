pipeline {
    agent any  // This allows Jenkins to run the pipeline on any available agent
    
    stages {
        stage('Build') {  
            steps {
                sh 'g++ -o output main/hello.cpp'  // error introduced
            }
        }
        
        stage('Test') {
            steps {
                sh './output'  // Executes the compiled C++ program
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'  // If any stage fails, print this message
        }
    }
}
