pipeline {
    agent any

    environment {
        FIREBASE_TOKEN = credentials('firebase-token') // stored in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                echo 'Nothing to build yet!'
            }
        }

        stage('Test') {
            steps {
                echo 'This is testing.'
            }
        }

        stage('Staging') {
            steps {
                echo 'Deploying to staging environment (placeholder)...'
            }
        }

        stage('Production') {
            steps {
                echo 'Deploying to Firebase Hosting...'
                sh 'firebase deploy --only hosting --project production --token $FIREBASE_TOKEN'
            }
        }
    }
}
