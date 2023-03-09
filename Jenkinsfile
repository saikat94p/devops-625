pipeline {
    agent any

    stages {
        stage('Fetch code') {
            steps {
               git branch: 'main', url: 'https://github.com/saikat94p/devops-625.git'
            }
        }
	  stage('Install Apache') {
            steps {
                sh 'sudo apt install apache2 -y'
            }
        }
	  stage('Deploy application') {
            steps {
                sh 'sudo cp -R * /var/www/html/'
            }
        }
    }
}
