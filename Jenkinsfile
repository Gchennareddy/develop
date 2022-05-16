#changes are updated in pipmaster branch
pipeline {
  agent any
  stages{
    stage ('checkout scm') {
        steps{
           checkout([$class: 'GitSCM', branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Gchennareddy/VProfile.git']]])
        }
    }
    stage ('build') {
        steps {
          sh "mvn package"
        }
    }
  }
}
    
