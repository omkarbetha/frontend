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
       curl -v -u admin:Omkar@123 --upload-file frontend.zip http://:8081/repository/frontend/frontend.zip
       '''
      }
    }
  }

}
