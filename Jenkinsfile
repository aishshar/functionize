// Lets Run this From Github

pipeline {
    agent { label 'jenkins-slave1' }
    stages {
          stage('Functionize-CLI') {
          agent {
              docker {
                image 'node:9.11.1'
                args  '-u root'
              }
          }
            steps {
              sh 'echo from Command $PROJECT_DEPLOYMENT_ID'
              sh 'echo from Command $YOUR_API_KEY'
              sh 'echo from Command $YOUR_API_KEY'
              sh 'rm -rf functionizecli'
              sh 'git clone https://functionize@bitbucket.org/functionize/functionizecli.git'
              sh 'cd functionizecli && npm install'
              sh 'cd functionizecli && npm install -g'
              sh 'cd functionizecli && wget -O - https://bitbucket.org/functionize/functionizecli/raw/master/ThirdParty_run.sh | bash'
            }
        }
    }
  }
