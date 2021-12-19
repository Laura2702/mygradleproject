pipeline {
  agent any
  stages {
    stage('Test1') {
      steps {
        readFile 'build.gradle'
        echo 'Hallo'
      }
    }

    stage('Mail') {
      steps {
        mail(subject: 'TestMail', body: 'Hi this is a test', to: 'l.pichlmeier1996@gmail.com', from: 'Laura')
      }
    }

  }
}