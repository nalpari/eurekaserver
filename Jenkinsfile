pipeline {
  agent any
  stages {
    stage('Initial') {
      steps {
        sh 'ls -al'
      }
    }
    stage('Build & Test') {
      steps {
        sh '/home/nalpari/apache-maven-3.6.1/bin/mvn clean package -Dmaven.test.skip=true'
      }
    }
    stage('Move jar') {
      steps {
        sh 'cp target/eurekaserver-0.0.1-SNAPSHOT.jar /home/jar'
      }
    }
  }
}