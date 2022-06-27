pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
          git(branch: 'main', url: 'https://github.com/NightmareAHouse/jenkins-test.git')
          sh 'bat 'npm install''
        }
      }

      stage('Test') {
        steps {
          sh 'bat 'npm install''
          sh 'bat 'npm run test''
        }
      }

      stage('Push') {
        steps {
          sh 'echo 'Pipeline end''
        }
      }
    }

    tools {
      nodejs 'node'
    }
}
