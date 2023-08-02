properties([pipelineTriggers([githubPush()])])
pipeline {
  agent any
  stages {
    stage('test') {
      agent any
      steps {
        echo 'Hello Webhook'
      }
    }
    stage('Checkout SCM') {
      steps {
        checkout([
          $class: 'GitSCM',
          branches: [[name: 'master']],
          userRemoteConfigs: [[
            url: 'https://github.com/DorraBenLetayfa/test.git',
            credentialsId: '',
          ]]
         ])
       }
}
    

  }
  environment {
    test = ''
  }
}
