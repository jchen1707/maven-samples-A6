pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/jchen1707/maven-samples-A6', branch: 'master')
      }
    }

    stage('clean') {
      steps {
        bat 'mvn clean'
      }
    }

    stage('test') {
      steps {
        bat 'mvn test'
      }
    }

    stage('verify') {
      steps {
        bat 'mvn verify'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}