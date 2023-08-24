pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your HTML source code from a Git repository
                checkout([$class: 'GitSCM', branches: [[name: 'master']], userRemoteConfigs: [[url: 'https://github.com/SwiftSoft-Bahadur/html.git']]])
            }
        }

        stage('Deploy HTML') {
            steps {
                // Copy your HTML files to a web server directory (e.g., Apache's webroot)
                sh "cp -r * /var/www/html"
            }
        }
    }
}
