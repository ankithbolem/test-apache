pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the feature/routelink branch
                echo "hello javahome"
            }
        }

        stage('Deploy to Apache on EC2') {
            steps {
                // SSH into the EC2 instance and deploy the code to the Apache document root
                script {
                   
                    echo "hi this a "
                }
            }
        }
    }
    
    post {
        always {
            echo 'Deployment completed!'
        }
    }
}
