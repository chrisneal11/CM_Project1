pipeline {
   agent any

     stages {

        stage('Clone Source') {
           steps {
                  git branch: 'master', url: 'https://github.com/chrisneal11/tomcat_test_app.git'	 
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
