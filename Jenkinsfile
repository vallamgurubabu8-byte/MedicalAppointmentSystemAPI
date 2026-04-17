pipeline {
agent any

stages {

    stage('Checkout') {
        steps {
            git 'https://github.com/vallamgurubabu8-byte/MedicalAppointmentSystemAPI.git'
        }
    }

    stage('Build') {
        steps {
            sh 'mvn clean package'
        }
    }

    stage('Test') {
        steps {
            sh 'mvn test'
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
