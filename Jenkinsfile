pipeline {
  agent any
  tools {
  jdk 'JAVA_HOME'
  maven 'MAVEN_HOME'
}

  stages {
    stage('GitHub project pull') {
      steps {
        git branch: 'main', url: 'https://github.com/damacharlamanisha/Jenkins.git'
      }
    }
    stage('mavenbuild'){
      steps {
        sh "mvn package -Dmaven.test.skip"
      }
    }
    stage('create zip'){
      steps {
        sh "zip -r target.zip target"
      }
    }
  }
}
