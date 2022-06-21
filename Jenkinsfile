pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        retry(count: 3) {
          echo 'Trying to Build'
        }

        echo 'Build Complete'
        retry(count: 3) {
          sh 'wwwwwwwww'
        }

      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Test stages Running'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deply?', ok: 'Yes, I am sure')
        echo 'Deploy Complete'
      }
    }

  }
}