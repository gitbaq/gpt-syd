//Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
//Some comment
pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'npm install'
            }
        }
        stage ('deliver'){
            steps{
                sh 'npm run build'
                sh 'npm start'
            }
        }
    }
}



