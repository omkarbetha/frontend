pipeline {
  agent any

  stages {
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
       Curl -v -u admin:Omkar@123 --upload-file frontend.zip http://172.31.4.7:8081/repository/frontend/frontend.zip

       '''
      }
    }
  }

}
