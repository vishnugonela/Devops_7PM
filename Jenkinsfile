pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        sh 'echo "Hello from STAGE1"'
      }
    }

    stage('Stage2') {
      parallel {
        stage('Stage2') {
          steps {
            sh 'echo "Hello from STAGE2"'
          }
        }

        stage('Parallel_stage1') {
          steps {
            sh 'echo "Hello from parallel stage1"'
          }
        }

        stage('Parallel_stage2') {
          steps {
            sh 'echo "From parallel stage2"'
          }
        }

      }
    }

  }
}