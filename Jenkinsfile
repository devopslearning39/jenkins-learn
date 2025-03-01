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

    // post build
sxasxas
    post { 
        failure { 
            echo 'This will works when build got failed'
        }
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'This is will works when build is successfully executed'
        }
    }
}