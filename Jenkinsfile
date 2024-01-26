pipeline {

    node {

        label "docker-node-alpine-agent"

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