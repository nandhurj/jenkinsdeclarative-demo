pipeline {
    agent any

    stages {
        stage('code') {
            steps {
                git 'https://github.com/learnsoftwares/maven_demo.git'
            }
        }
         stage('build') {
            steps {
                bat 'mvn clean package'
            }
        }
         stage('deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '91fddd5c-c130-4875-89ee-ec93dbc71add', path: '', url: 'http://localhost:9090/')], contextPath: '**/*.war', war: ''
            }
        }
    }
}





