pipeline{
    agent{
        docker {
            image "post/newman"
            args "--entrypoint=''"
        }
    }
    stages{
         stage('Test API'){
            steps{
                sh 'newman --version'
            }
        }
        stage('Test API'){
            steps{
                sh 'newman run collections/collection.json -e environment -r cli,junit --reporter-junit-export="newman-report.xml"'
            }
        }
    }
}