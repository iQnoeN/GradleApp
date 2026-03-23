pipeline {
  agent any
  tools {
    jdk "JDK"
    gradle "Gradle"
  }
  stages {
    stage('Checkout') {
      git branch:'main' , url:'https://github.com/iQnoeN/GradleApp.git'
    }
    stage('Build') {
      sh 'gradle build'
    }
    stage('Test') {
      sh 'gradle test'
    }
    stage('Run Application') {
      sh'gradle run'
    }
  }
  post {
    success {
      echo "Build Success"
    }
    failure {
      echo "Build Failure"
    }
  }
}
