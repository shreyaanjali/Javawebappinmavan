pipeline{
    agent any
    stages{
        stage("Sonar-Quality-check"){
            agent{
                docker { 
                    image 'openjdk:11'
                }
            }
            steps{
                scripts{
                    withSonarQubeEnv(credentialsId: 'Sonar-password-token') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
                    }
                }
            }
    
        }
    }
}
