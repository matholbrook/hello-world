pipeline {
  agent {
    node {
      label '127.0.0.1'
    }

  }
  stages {
    stage('stage1') {
      steps {
        sh '''#!/bin/bash
echo "this is stage one"'''
      }
    }
  }
  environment {
    node = 'localhost'
  }
}