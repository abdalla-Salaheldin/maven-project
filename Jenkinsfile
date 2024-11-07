pipeline {
    agent any 
    stages {
        stage('SCM Checkout: Download code from GitHub') {
            steps {
                git branch: 'master', url: 'https://github.com/abdalla-Salaheldin/maven-project.git'
            }
        }
        
        stage('Execute Unit Test Framework') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn test'
                }
            }
        }
    }
}
