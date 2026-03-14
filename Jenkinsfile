pipeline {

    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/vishalab26/crm-devops-project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'cd app && mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t vishalmath2605/crm-app:1.0 .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker push vishalmath2605/crm-app:1.0'
            }
        }

    }

}
