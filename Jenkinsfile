pipeline {
    agent any
    stage('Preparation: Clean') {
        when {
          anyOf {
            branch 'master'
            changeRequest()
          }
        }
        steps {
          sh "rm -rf /var/lib/jenkins/.gradle/caches"
          sh "${WORKSPACE}/gradlew clean"
          echo "******* ${WORKSPACE}"
        }
      }
}