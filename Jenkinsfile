pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Starting deployment'
      }
    }

    stage('Deployment') {
      parallel {
        stage('Deployment') {
          steps {
            sh '''#!/bin/bash

ssh -tt root@192.168.0.35 \'
ls -ltr\''''
          }
        }

        stage('test') {
          steps {
            isUnix()
          }
        }

      }
    }

    stage('finish') {
      steps {
        echo 'we are done'
      }
    }

  }
  environment {
    IBM = 'IIB and MQ Deployment'
  }
}