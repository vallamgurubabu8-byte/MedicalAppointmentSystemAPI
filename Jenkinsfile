pipeline{
    agent any
    tools{
        maven 'Maven3'
        jdk 'JDK21'
    }
    stages{
      stage('Checkout'){
            steps{
                git branch: 'master', url: ''
            }
        }
        stage('Build'){
            steps{
                sh 'mvn claen package'
            }
        }
        stage('Build'){
            steps{
                 sh 'mvn claen package'
            }
        }
    }

    post{
        success {
            echo 'Build Successfull'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}