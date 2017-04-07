pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            echo 'Building..'
            
          },
          "announce": {
            sh 'echo "doing things"'
            
          },
          "think": {
            sleep(unit: 'MILLISECONDS', time: 200)
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}