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
                sh "xcopy C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\jenkins_prac D:\\Jenkins_prac /E /I /Y"
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