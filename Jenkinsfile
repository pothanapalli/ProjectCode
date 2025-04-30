pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'github-pat-id', url: 'https://github.com/your-username/your-repo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'No build step needed for plain HTML.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static website...'
                // Simulate deployment (e.g., copy to /var/www/html if on a server)
                sh 'mkdir -p /tmp/deploy && cp *.html /tmp/deploy/'
            }
        }
    }

    post {
        success {
            echo 'Website deployed successfully.'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}
