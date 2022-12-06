pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/dstribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs 3.6.3'
  }
  post {
    always {
      echo 'this is my first pipeline - yaaayyy'
    }

  }
}