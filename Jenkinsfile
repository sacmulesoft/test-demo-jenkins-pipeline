pipeline {

  agent any

  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "*******updated Munit test cases execution ********"
      }
    }

     stage('Deployment') {

      steps {
            bat 'mvn -U -V -e -B -DSkipTests -PSandbox deploy -DmuleDeploy'
      }
    }

  }
}