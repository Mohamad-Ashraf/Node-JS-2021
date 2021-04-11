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

    stage('error') {
      steps {
        sh '''#!/bin/bash
if [ oc get dc --show-labels | grep "app=drupal" | cut -d" " -f3==1 ] ; then
 echo "DC Exist"
else
 echo "DC Doesn\'t Exist"
fi'''
      }
    }

  }
}