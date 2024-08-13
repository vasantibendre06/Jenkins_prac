pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Building the project...'
            }
        }
        stage('Copy'){
            steps{
                sh "xcopy /s /y C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\jenkins_prac C:\\inetpub\\wwwroot\\Jenkins_prac"
            }
        }
        stage('Test'){
            steps{
                echo 'Testing the project...'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying the project...'
            }
        }
    }
}