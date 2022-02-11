pipeline {
    agent any

    stages {
        stage('continous DOwnloading') {
            steps {
                git 'https://github.com/3Himala/war-web-project.git'
            }
        }
        stage('continous build') {
            steps {
                sh 'mvn install'
            }
        }
      stage('continous deploy') {
            steps {
                sh 'sshpass -p "himala" scp target/wwp-1.0.0.war himala@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }  
    }
}
