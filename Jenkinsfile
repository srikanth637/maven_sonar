pipeline {
    agent any
    environment {
        PATH = "/opt/maven/bin:${PATH}"
    }
    stages{
    stage("collect code from git"){
            steps{
            git credentialsId: 'git_credentials', url:'https://github.com/srikanth637/maven_sonar.git'
           }
        }    
        stage("build code"){
            steps{
            sh "mvn install" 
            }
        }
        stage("unit test") {
            steps{
                sh "mvn test"
            }
        }
    }
}
