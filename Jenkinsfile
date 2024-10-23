pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
            steps {
                echo "Checking out from Git Repo"
                git 'https://github.com/arjun-s-XL/Pipeline_Script.git'
            }
        }
        stage('Build') {
            steps {
                echo "Building the checked-out project!"
                sh './Build.sh'  
            }
        }
        stage("Unit-Test") {
            steps {
                echo "Unit testing the checked-out project!"
                sh './Unit.sh'  
            }
        }
        stage("Quality") {
            steps {
                echo "Quality Assurance of checked-out project!"
                sh './Quality.sh'  
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying the checked-out project!"
                sh './Deploy.sh'  
            }
        }
    }
    post {
        always {
            echo 'This will always run, regardless of the pipeline result.'
        }
        success {
            echo 'Pipeline succeeded! Notify the team or trigger other jobs.'
        }
        failure {
            echo 'Pipeline failed! Alert the team or initiate rollback steps.'
        }
    }
}

