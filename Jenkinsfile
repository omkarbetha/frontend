pipeline {
  agent {
    label 'NODEJS'
    }

  stages {

    stage('Download Dependencies') {
      steps {
      sh '''
      npm install
      '''
      }
    }
    stage('Prepare Artifacts') {
       steps {
       sh '''
         zip -r ../frontend.zip *
       '''
       }
    }
    stage('Upload Artifacts') {
      steps {
       sh '''
       curl -f -v -u admin:Omkar@123 --upload-file /home/ubuntu/workspace/frontend.zip http://172.31.4.7:8081/repository/frontend/frontend.zip
       '''
      }
    }
  }
}
