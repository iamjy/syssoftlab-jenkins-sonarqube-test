node { 
  stage('SCM') { 
    checkout scm 
  } 

  stage('SonarQube Analysis') { 
    def scannerHome = tool 'SonarScanner'; 
    withSonarQubeEnv() { 
      sh """
        ${scannerHome}/bin/sonar-scanner \
          -Dsonar.projectKey=iamjy_syssoftlab-jenkins-sonarqube-test_AZO5bNje2pBDTwJG71T1 \
          -Dsonar.login=sqa_5c06dc3b67cb743ebe4dabcf91b035955d351da9
        """
    }
  }
}
