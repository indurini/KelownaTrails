// NOTE for Students:
//
// In this example, Firebase is being used securely using Jenkins credentials.
// For real projects (production CI/CD), you must NOT hardcode Firebase login.
// Instead, store your Firebase token or service account key in Jenkins Credentials
// (e.g., "Secret Text" or "Secret File") and load it as an environment variable.
// Example: withCredentials([string(credentialsId: 'firebase-token',
pipeline {
    agent any

    environment {
        FIREBASE_TOKEN = credentials('firebase-token')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Nothing to do!'
            }
        }

        stage('Test') {
            steps {
                echo 'This is testing.'
            }
        }

        stage('Staging') {
            steps {
                echo 'This is Staging.'
            }
        }

        stage('Production') {
            steps {
                echo 'Deploying to Firebase Hosting...'
                sh 'firebase use my-webapp-testing'
                sh 'firebase deploy --only hosting --token $FIREBASE_TOKEN'
            }
        }
    }
}


