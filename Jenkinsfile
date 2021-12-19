pipeline {
  agent any
  stages {
    stage('Log Tool Version') {
      parallel {
        stage('Log Tool Version') {
          steps {
            sh '''git --version
java -version
gradle -version'''
          }
        }

        stage('Check for build') {
          steps {
            fileExists 'build.gradle'
          }
        }

      }
    }

    stage('Build with Gradle') {
      steps {
        sh 'gradle build'
      }
    }

    stage('Post Build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Hey, it worked!')
      }
    }

  }
}