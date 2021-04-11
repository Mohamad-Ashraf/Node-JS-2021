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
        openshiftVerifyDeployment(depCfg: 'drupal', apiURL: 'https://api.ocp.rscloud.io:6443')
      }
    }

    stage('Output') {
      steps {
        echo 'It works FINE'
      }
    }

  }
}