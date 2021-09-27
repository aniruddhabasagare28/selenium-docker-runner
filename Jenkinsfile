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
            archiveArtifacts artifacts: 'test-output/**'
             bat "docker-compose down"
        }
    }
}