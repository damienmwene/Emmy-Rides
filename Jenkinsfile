pipeline {

    agent any

        triggers {
            pollscm "* * * * *"
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