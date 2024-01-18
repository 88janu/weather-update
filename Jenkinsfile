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
                sh 'scp /home/slave1/workspace/bus-bookin_develop/target/bus-booking-app-1.0-SNAPSHOT.jar root@172.31.6.180:/opt/apache-tomcat-8.5.98/webapps'
            }
        }
    }
}
