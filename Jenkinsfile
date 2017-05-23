#!/usr/bin/env groovy

node {
    stage('Example') {
        steps {
            echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
        }
    }
    environment { 
        CC = 'clang'
    }
    stage('Example2') {
        environment { 
            DEBUG_FLAGS = '-g'
        }
        steps {
            sh 'printenv'
        }
    }
    stage('Build') {
        echo 'Building....'
    }
    stage('Test') {
        echo 'Building....'
    }
    stage('Deploy') {
        when {
            expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
            }
        }
        steps {
            echo 'Deploying....'
        }
    }
}