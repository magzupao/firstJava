pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '11b51bc8b772dd91a8049eb1f1a00835675f6e8f', url: 'https://github.com/magzupao/firstJava.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                javac HelloWorld.java
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
