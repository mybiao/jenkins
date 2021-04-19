pipeline{
    agent{
        docker {image 'go:1.16'}
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
