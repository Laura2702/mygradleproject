pipeline {
  agent any
  stages {
    stage('Test1') {
      steps {
        readFile 'build.gradle'
        echo 'Hallo'
      }
    }

    stage('file') {
      steps {
        fileExists 'gradle-wrapper.jar'
      }
    }

    stage('build') {
      steps {
        withGradle() {
          build 'build'
        }

      }
    }

  }
}