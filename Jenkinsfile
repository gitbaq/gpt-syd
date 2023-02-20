//Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
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
                npm install
            }
        }
        stage ('deliver'){
            steps{
                npm run build
                npm start
            }
        }
    }
}



