pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
               echo "Building"
                sh "g++ /Server/server.cpp"
                sh "g++ /Client/client.cpp"
            }
        }
        stage('Test'){
            steps{
                echo "testing"
                sh "g++ -o main.cpp"
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
