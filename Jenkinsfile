pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        tidy -q -e *.html
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-2', credentials:'aws-static') {
        // do something
            s3Upload(file:'index.html', bucket:'pipline-bucket', path:'')
            }
      }
    }
  }
}
    
