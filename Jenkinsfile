pipeline {
  agent { label 'jenkins_slave' }
  stages {
    stage('start') {
      steps {
        script {
        withCredentials([usernamePassword(credentialsId: 'dockerhub-credentials', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
          sh """
              docker login -u ${USERNAME} -p ${PASSWORD}
              docker build -t ahmedsalahh12/react .
              docker push ahmedsalahh12/reatct
          """
        }
        
      }
      }
      
    }
    stage('Deploy') {
      steps {
       script {
        
        }
        
      }
      }
    }
  }
}
