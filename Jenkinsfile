pipeline {
  agent any
  parameters {
  choice choices: ['dev', 'prod'], description: 'select the environment', name: 'ENV'
  }
  environment {
  JAVA_VERSION = "1.2.19"
  }
  stages {
    stage('Working with variables') {
      steps {
        script {
          // declaring user-defined variables
          Money=500
          //accessing values of a variables
          println "the money value given is ${Money}"

          // consuming pre-defined variables
          println "my curent execution folder is ${WORKSPACE}"
          println "the name of my selected git branch is ${GIT_BRANCH}"
          println "the home-directory of my jenkins is ${JENKINS_HOME}"

          // consuming parameter variables
          println "my selected environment is ${params.ENV}"

          // consuming environment variables
          println "my selected java version is ${env.JAVA_VERSION}"
        }
      }
    }
  }  
}
