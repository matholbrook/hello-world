pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          agent any
          steps {
            sh '''#!/bin/bash
echo "this is stage one"
FOO=BAR'''
          }
        }
        stage('stage1b') {
          steps {
            sh '''#!/bin/bash
echo "this is stage oneB"'''
          }
        }
      }
    }
  }
}