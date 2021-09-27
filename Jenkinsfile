pipeline{
    agent any
    stages{
        stage("Start GTID"){
            steps{
                bat "docker-compose up -d hub chrome firefox"
            }
        }
        stage("RUN TESt"){
            steps{
                bat "docker-compose up search-model"
            }
        }
    }
    post{
        always{
            archiveArtifacts artifacts: 'search-result/**'
             bat "docker-compose down"
        }
    }
}