pipeline{
    agent none
    stages{
        stage("build"){
            agent{
                docker {image 'golang:1.16'}
            }
            steps{
                sh 'go build -o demo'
            }
        }
        stage('run'){
            agent any
            steps{
                sh './demo'
                sh 'echo "end"'
            }
        }

        stage("maven"){
            agent {
                docker {image 'maven:3.8-openjdk-11'}
            }
            steps{
                sh 'mvn -version'
            }
        }
    }
}
