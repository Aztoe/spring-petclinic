pipeline {
      agent any

      stages {
          stage('Checkout') {
              steps {
                  echo '코드 가져오는 중...'
                  checkout scm
              }
          }
          stage('Build') {
              steps {
                  echo '빌드 중...'
                  sh './mvnw clean package -DskipTests'
              }
          }
          stage('Test') {
              steps {
                  echo '테스트 중...'
                  sh './mvnw test'
              }
          }
      }
  }
