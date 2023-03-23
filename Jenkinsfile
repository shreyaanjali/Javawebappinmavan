pipeline{
    agent any
    stages{
        stage("Sonar-Quality-check"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonarqube-tocken-password' , installationName: 'SonarQubeServer') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
                    }
                }
            }
    
        }
    }
}
