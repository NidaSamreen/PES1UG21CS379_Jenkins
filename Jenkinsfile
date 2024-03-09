pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                ech "This is Build stage."
                build 'PES1UG21CS379-1'
                sh 'g++ ./main1.cpp -o output'
                echo "Build Stage Successful"
            }
        }
        stage('Test') { 
            steps {
                echo "This is Test stage." 
                sh './output'
                echo "Test Stage Successful"
            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy stage."
                echo "Deployment Success"
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}
