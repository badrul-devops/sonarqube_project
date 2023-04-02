pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/badrul-devops/sonarqube_project.git'
            }
        }
        stage('build docker image'){
            steps{
                sh 'docker build -t sonarqube_project .'
            }
        }
        stage('run docker image'){
            steps{
                sh 'docker run -d -p 8000:8000 sonarqube_project'
            }
        }


    }
}