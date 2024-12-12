node { 
  stage('SCM') { 
    checkout scm 
  } 

  stage('SonarQube Analysis') { 
    def scannerHome = tool 'SonarScanner'; 
    withSonarQubeEnv() { 
      sh """
        ${scannerHome}/bin/sonar-scanner
          -Dsonar.login=sqa_5c06dc3b67cb743ebe4dabcf91b035955d351da9
        """
    }
  }
}
