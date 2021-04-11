pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        sh '''#!/bin/bash
ls -la
oc get pods'''
      }
    }

    stage('Check if DC exist') {
      steps {
        openshiftVerifyDeployment 'drupal'
      }
    }

    stage('Output') {
      steps {
        echo 'It works FINE'
      }
    }

  }
}