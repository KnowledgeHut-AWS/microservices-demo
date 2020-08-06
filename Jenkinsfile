pipeline {
  agent {
    docker {
      image 'bryandollery/terraform-packer-aws-alpine'
      args '-v /run/docker.sock:/run/docker.sock'
    }

  }
  stages {
    stage('build') {
      agent {
        docker {
          image 'alpine'
          args '-v /run/docker.sock:/run/docker.sock'
        }

      }
      steps {
        sh '''#!/bin/bash
echo "Hello World"'''
      }
    }

    stage('test') {
      agent {
        docker {
          image 'alpine'
          args '-v /run/docker.sock:/run/docker.sock'
        }

      }
      steps {
        echo 'Hello Testers'
      }
    }

    stage('release') {
      agent {
        docker {
          image 'alpine'
          args '-v /run/docker.sock:/run/docker.sock'
        }

      }
      steps {
        sh '''#!/bin/bash
echo "release"'''
      }
    }

  }
  environment {
    TF_NAMESPACE = 'bryan'
  }
}