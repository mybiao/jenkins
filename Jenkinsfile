pipeline{
    agent{
        docker {image 'go:1.15.7'}
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