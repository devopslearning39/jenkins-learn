pipeline {
    agent {
        node {
            label 'jenkins-agent1'
        }
    }
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'HOURS')

        // Disables concurrent builds
        disableConcurrentBuilds()
    }
    environment { 
        course = 'DevOps With AWS'
    }
    stages {
        stage('Build') {
            steps {
                echo "We are learning $course"
                echo "We have configured github webhook as well...."
                echo "this is building"
                sleep(20)
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