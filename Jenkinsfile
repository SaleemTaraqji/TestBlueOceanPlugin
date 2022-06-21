pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Complete'
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