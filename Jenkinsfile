pipeline {
  agent {
    label 'java8 && proant'
  }
  stages {
    stage('Build') {
      steps {
        sh 'proant init'
        sh 'proant dist'
      }
    }
    stage('Test') {
      when { expression { false } }
      steps {
        echo 'Testing...'
      }
    }
    stage('Analyze') {
      when { expression { false } }
      steps {
        echo 'analyzing...'
      }
    }
    stage('Archive') {
      when { environment name: 'BRANCH_NAME', value: 'master' }
      steps {
        echo 'Archiving (placeholder)...'
        /* sh 'proant deploy-only' */
      }
    }
  }
}
