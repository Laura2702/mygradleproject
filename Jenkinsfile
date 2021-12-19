pipeline {
  agent any
  stages {
    stage('Test1') {
      steps {
        readFile 'build.gradle'
        echo 'Hallo'
        withGradle() {
          sh 'gradlew build'
        }

      }
    }

  }
}