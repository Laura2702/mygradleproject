pipeline {
  agent any
  stages {
    stage('Log Tool Version') {
      parallel {
        stage('Log Tool Version') {
          steps {
            bat 'logversion.bat'
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
        bat 'build.bat'
      }
    }

    stage('Post Build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Hey, it worked!')
      }
    }

  }
}