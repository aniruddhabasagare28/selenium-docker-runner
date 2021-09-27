pipeline{
    agent any
    stages{
        stage("RUN TEST"){
            steps{
                sh "docker-compose up"
            }
        }
        stage("BRING GRID DOWN"){
            steps{
                sh "docker-compse down"
            }
        }
    }
}