pipeline {
  agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
  }
  
  environment {
        CI = 'true'
    }
  
    stages {
      stage('Build') {
        steps {
          git(branch: 'main', url: 'https://github.com/NightmareAHouse/jenkins-test.git')
         bat 'npm install'
        }
      }

      stage('Test') {
        steps {
          bat 'npm install'
          bat 'npm run test'
        }
      }

      stage('Push') {
        steps {
          echo 'Pipeline end'
        }
      }
    }

    tools {
      nodejs 'node'
    }
}
