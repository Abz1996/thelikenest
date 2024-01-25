pipeline {
    agent any
    stages {

        stage("build & SonarQube analysis") {          
            steps {
                    withSonarQubeEnv('Sonarserver') {
                        sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=Abz1996_thelikenest'
             
            }
        }
    }
    }
    
    tools{
      maven 'M2_HOME'
    }
     stages{
      stage('clean'){
       steps {
         sh 'mvn clean'
       }
    }
    stage('compile'){
      steps{
        sh 'mvn compile'
      }
    }
    stage('install'){
      steps{
        sh 'mvn install'
        sh 'mvn package'

      }
    }
    
    }

}
