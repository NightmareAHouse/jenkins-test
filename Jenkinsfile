pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(branch: 'main', url: 'https://github.com/NightmareAHouse/jenkins-test.git')
        bat 'npm install'
      }
    }
  }
  stages {
    stage('Test') {
      steps {
        bat 'npm install'
        bat 'npm run test'
      }
    }
  }

    stages {
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
