// Jenkins Pipeline for KelownaTrails
// NOTE for Students:
// Firebase is deployed securely using Jenkins credentials.
// Store your Firebase token as a Secret Text in Jenkins with ID "firebase-token".

pipeline {
    agent any

    environment {
        FIREBASE_TOKEN = credentials('firebase-token')   // Secret Text in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                echo 'Nothing to build yet!'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
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
                // Direct deploy with --project avoids firebase use/.firebaserc issues
                sh 'firebase deploy --only hosting --project my-webapp-testing --token $FIREBASE_TOKEN'
            }
        }
    }
}
