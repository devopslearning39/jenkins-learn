pipeline {
    agent {
    node {
        label 'jenkins-agent1'
    }
}
    stages {
        stage('Build') {
            steps {
                echo "this is building"
            }
        }
        stage('Test') {
            steps {
               echo "this is testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "this is deploying"
            }
        }
    }
}