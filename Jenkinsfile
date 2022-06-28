pipeline {
  agent any
  
  environment {
        CI = 'true'
    }
  
    stages {
      stage('Build') {
        steps {
          git(branch: 'main', url: 'https://github.com/NightmareAHouse/jenkins-test.git')
         sh  'npm install'
        }
      }

      stage('Test') {
        steps {
          sh  'npm install'
          sh  'npm run test'
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
