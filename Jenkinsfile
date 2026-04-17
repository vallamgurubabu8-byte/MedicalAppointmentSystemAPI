pipeline {
agent any

stages {

    stage('Checkout') {
        steps {
            git branch: 'main', url: 'https://github.com/vallamgurubabu8-byte/MedicalAppointmentSystemAPI.git'
        }
    }

    stage('Build') {
        steps {
            bat 'mvn clean package'
        }
    }

    stage('Test') {
        steps {
            bat 'mvn test'
        }
    }
}

post {
    success {
        echo '✅ Build Successful!'
    }
    failure {
        echo '❌ Build Failed!'
    }
}
}
