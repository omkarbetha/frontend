pipeline {
  agent any

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
       curl -v -u admin:Omkar@123 --upload-file /var/lib/jenkins/workspace/frontend.zip http://172.31.4.7:8081/repository/frontend/frontend.zip.1
       '''
      }
    }
  }
}
