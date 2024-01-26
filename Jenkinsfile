pipeline {

    agent {

        label "docker-node-alpine"

    }

    triggers {
        pollSCM "* * * * *"
    }

    environment {

        CI = false //do not treat errors as warnings

    }

    stages {

        stage ('build') {
            steps {
                echo "building the application"
                sh '''
                npm install
                npm run build
                '''
            }

        }

    }

}