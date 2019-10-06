
pipeline {
     agent { label 'master' }
     tools {
          maven 'Maven 3.6.2'
     }
     stages {
          stage('Source') {
               steps {
                    git branch: 'master',
                         url: 'https://github.com/ladyusa/evoting.git'
               }
          }
          stage('Build') {
               steps {
                    sh 'mvn compile'
               }
          }
          stage('Test') {
               steps {
                    sh 'mvn test'
               }
          }
          stage('Deploy') {
               steps {
                    sh 'mvn spring-boot:run'
               }
          }
     }
}
