pipeline{
    agent{
        docker {image 'golang:1.16'}
    }

    stages{
        stage("build"){
            steps{
                sh 'go build .'
            }
        }
        stage('run'){
            steps{
                sh 'go run .'
            }
        }
    }
}
