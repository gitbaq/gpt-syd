//Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    //agent { docker { image 'node:16.17.1-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'npm start'
            }
        }
        stage ('deliver'){
            set -x
            npm run build
            npm start
            set +x
        }
    }
}


