pipeline {
  agent any
  stages {
    stage('Log tool Version') {
      parallel {
        stage('Log tool Version') {
          steps {
            sh '''mvn --version
git --version
java -version'''
          }
        }

        stage('check for yashwanth') {
          steps {
            fileExists 'yashwanth'
          }
        }

      }
    }

    stage('Build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('post build steps') {
      steps {
        writeFile(file: 'Result.txt', text: 'It Worked')
      }
    }

  }
}