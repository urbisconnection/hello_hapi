#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'ubuntu'
            label 'docker'
            args '-v /tmp:/tmp'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
