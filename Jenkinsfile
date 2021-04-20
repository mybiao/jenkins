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
    }
}
