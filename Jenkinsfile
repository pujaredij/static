pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-2') {
        // do something
            s3Upload(file:'index.html', bucket:'pipline-bucket', path:'')
            }
      }
    }
  }
}
    
