pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS377-1 error.cpp' //new.cpp will give the correct output
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS377-1'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
