pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
         steps {
             sh "chmod 777 -R /var/lib/jenkins/workspace/azure-voting-app-redis"
            sh(script: 'docker compose build')
         }
      }
   }
}
