pipeline {
  agent any
  stages {
    stage('Stage 1') {
      parallel {
        stage('Stage 1') {
          steps {
            echo 'Hello Stage 1 step 1'
            sleep 10
            echo 'Stage 1 step 3 after 10 seconds'
          }
        }

        stage('PStage1') {
          steps {
            echo 'PStage 1 step 1'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sh 'echo "Hello: Deploy"'
            echo 'After Deploy'
            sleep 10
          }
        }

        stage('Watch Logs') {
          steps {
            echo 'Deployment logs'
          }
        }

      }
    }

  }
}