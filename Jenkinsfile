pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/n-chandana1419/calculator-Build1'
            }
        }
        stage('Maven Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }
        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', allowEmptyArchive: true
            }
        }
    }
}
