
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
                sh 'firebase use production'
                sh 'firebase deploy --only hosting --token $FIREBASE_TOKEN'
            }
        }
    }
}
