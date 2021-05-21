pipeline {
   agent any

   stages {
      stage('checkout') {
         steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/sameena-ops/TW_Bootcamp_QA']]])
         }
      }

      stage('Maven installation') {
         steps {
             sh 'mvn -f Bootcamp_UI/pom.xml clean test'
        }
      }
   }
}
