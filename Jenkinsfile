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

        stage("Fix Ansible/Python Issue") { 
           steps {
                  sh "sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 1"
                  sh "sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 2"
                 }

        stage("Deploy Package") {
           steps {
                  sh ""
                  sh ""
                  sh "ansible --version"
                 }
        }
     }
}
