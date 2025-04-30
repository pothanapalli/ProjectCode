pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        sh '''
          mkdir -p /var/www/html/pothanapalli
          cp DevopsProjectCode.html /var/www/html/pothanapalli/index.html
        '''
      }
    }
  }
  post {
    success {
      echo "Access your file at: http://localhost/web/pothanapalli/index.html"
    }
  }
}
