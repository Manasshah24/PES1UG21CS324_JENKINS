pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Your build steps here
                build 'PES1UG21CS324'
                sh 'g++ main1.cpp -o output'
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                // Your test steps here
                sh './output'
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                // Your deployment steps here
                echo 'deploy'
                
            }
        }
    }

    post {
        failure{
            // Display 'pipeline failed' if any previous stage failed
            error 'Pipeline failed'
        }
    }
}
