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
        waitUntil() {
          sh '''#!/bin/bash
oc get dc --show-labels | grep "app=drupal"'''
        }

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