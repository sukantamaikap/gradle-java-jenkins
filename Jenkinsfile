pipeline {
    agent any
    stages {
    stage('Preparation: Clean') {
        steps {
          sh "rm -rf /var/lib/jenkins/.gradle/caches"
          sh "${WORKSPACE}/gradlew clean"
          echo "******* ${WORKSPACE}"
        }
      }
    }
}