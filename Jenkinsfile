pipeline{
    agent any
    environment {
        APACHE_ROOT = '/var/www/html'
    }
    
    stages{
        stage('Admin'){
            steps{
                sh 'whoami'
                sh 'sudo -i'
            }
        }
        
        stage('Build'){
            steps{
                echo 'Building the project...'
            }
        }

        stage('Checkout') {
            steps {
                git url: 'https://github.com/vasantibendre06/Jenkins_prac.git', branch: 'main'
            }
        }

        stage('Deploy'){
            steps{
                sh "sudo cp -r ./ /var/www/html"
                sh 'sudo systemctl restart apache2'
            }
        }
    }

    post {
        success {
            echo 'Deployment completed successfully!'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}
