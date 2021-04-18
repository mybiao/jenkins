pipeline{
    agent{
        docker {image 'go:1.15.7'}
    }

    stages{
        stage("build"){
            step{
                sh 'go build .'
            }
        }
        stage('run'){
            step{
                sh 'go run .'
            }
        }
    }
}