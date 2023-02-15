pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
               echo "Building"
                sh "script.sh"
            }
        }
        stage('Test'){
            steps{
                echo "testing"
                sh "g++ main.cpp"
                sh "./a.out"
            }
        }
        stage('Deploy'){
            steps{
            echo "Task Completed"
            }
        }
    }
}
