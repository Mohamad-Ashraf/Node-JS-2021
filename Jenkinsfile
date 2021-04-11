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

    stage('Output') {
      steps {
        echo 'It works FINE'
      }
    }

  }
}