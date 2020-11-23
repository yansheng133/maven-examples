stage('Sonarqube'){
  agent any
  when{
    branch 'master'
  }
  environment{
    sonarpath = tool 'SonarScanner'
  }
  steps{
    echo 'Running Sonarqube Analysis...'
      withSonarQubeEnv('sonar'){
        sh "${sonarpath}/bin/sonar-scanner -Dproject.setting=sonar-project.properties"
      }
  }
}
