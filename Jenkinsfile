pipeline {
    agent any

    tools {
    maven 'maven'
}
    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/MyMavenSeleniumApp01.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Run Selenium Test') {
            steps {
                sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
            }
        }

    }
}
