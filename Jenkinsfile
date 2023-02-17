pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS221-1 sample1.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh "./main/sample1.cpp"
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
