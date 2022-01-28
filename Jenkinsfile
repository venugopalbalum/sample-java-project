pipeline {
    agent {
        docker {
            image 'cameronmcnz/ant-jdk8-git:latest'
            
        }
     }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ant clean compile test package war'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo " Workspace ${env.WORKSPACE} exec ${env.EXECUTOR_NUMBER}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
