#changes are updated in pipmaster branch
pipeline {
  agent any
  stages{
    stage ('checkout scm') {
        steps{
           checkout([$class: 'GitSCM', branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Gchennareddy/VProfile.git']]])
           env.LATEST_COMMITER = sh(script: 'git show -s --format=\'%ae\'',returnStdout: true).trim()
        }
    }
    stage ('build') {
        steps {
          sh "mvn package"
        }
    }
  }
}
    
