pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the feature/routelink branch
                git branch: 'feature/routelink', url: 'https://github.com/your-username/sample-apache-app.git'
            }
        }

        stage('Deploy to Apache on EC2') {
            steps {
                // SSH into the EC2 instance and deploy the code to the Apache document root
                script {
                    sh '''
                    ssh -o StrictHostKeyChecking=no ec2-user@<jenkins-test-ec2-ip> << 'EOF'
                    cd /var/www/html
                    sudo git pull origin feature/routelink
                    sudo systemctl restart httpd  # Restart Apache to reflect changes
                    exit
                    EOF
                    '''
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
