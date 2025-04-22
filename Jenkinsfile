pipeline {
        agent none
        stages {
         
          stage("build & sonarqube") {
            agent any
            steps {
              withSonarQubeEnv('Sonar-token') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
