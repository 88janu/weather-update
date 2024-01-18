pipeline {
    agent {label 'slave1'}
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf weather-update'
                sh 'git clone https://github.com/88janu/weather-update.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
        stage('deploy') {
            steps {
                sh 'echo "hi"'
                //sh ' root@172.31.6.180:/opt/apache-tomcat-8.5.98/webapps'
            }
        }
    }
}
