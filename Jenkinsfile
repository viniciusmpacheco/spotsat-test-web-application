pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                parallel(
                  "unit-test": {
                    echo 'Unit Testing..'
                  },
                  "integration-test": {
                    echo 'Integration Testing..'
                  },
                  "functional-test": {
                    echo 'Functional Testing..'
                  }
                )
            }
        }
        stage('Delivery') {
            steps {
                echo 'Delivering..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}