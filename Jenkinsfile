pipeline {
   agent any

     stages {

        stage('Clone Source') {
           steps {
                  git branch: 'main', url: 'https://github.com/chrisneal11/tomcat_test_app'
                 }
        }

        stage("Build Source") {          	 
           steps {
                  sh "mvn clean package"
                 }
        }

        stage("Deploy Package") {
           steps {
                  sh "ansible --version"
                 }
        }
     }
}
