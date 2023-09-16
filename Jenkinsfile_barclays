pipeline {
  agent any 
  tools{
    maven "maven386"
  }
  stages{
       stage('1GetCode') {
            steps{
              git branch: 'dev', url: 'https://github.com/benadaba/maven-web-application-jf'
                }

        }
      
       stage('2build') {
            steps{
              sh "mvn package"
            }
        }
        /*
     stage('3CodeQualityAnalysis') {
            steps{
              sh "mvn sonar:sonar"
            }
        }
        */
        
     stage('deploy') {
            steps{
              sh "mvn deploy"
            }
        }
    }
    
    post{
        always{sh "echo always"}
        success{sh "echo success"}
        failure{sh "echo failure"}
    }
}

