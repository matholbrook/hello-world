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
echo "this is stage oneB"
echo "FOO = ${FOO}"'''
          }
        }
      }
    }
    stage('stage2') {
      parallel {
        stage('stage2') {
          steps {
            sh '''#!/bin/bash
echo "this is stage2"'''
          }
        }
        stage('stage2b') {
          steps {
            echo 'HELLO!'
          }
        }
      }
    }
    stage('stage3') {
      steps {
        sh '''#!/bin/bash
date'''
      }
    }
  }
}