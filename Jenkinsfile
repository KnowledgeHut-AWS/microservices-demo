pipeline {
  agent {
    docker {
      image 'bryandollery/terraform-packer-aws-alpine'
    }

  }
  stages {
    stage('build') {
      agent {
        docker {
          image 'alpine'
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