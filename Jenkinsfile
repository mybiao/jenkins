pipeline{
    agent{
        docker {image 'golang:1.16'}
    }

    stages{
        stage("build"){
            steps{
                sh 'go build -o demo'
            }
        }
        stage('run'){
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
