pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/jchen1707/maven-samples-A6', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('clean and test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}