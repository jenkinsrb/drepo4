pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello build'
            }
        }
        stage('test') {
            parallel {
              stage('unit test') { 
                steps {
                echo 'Hello unit test'
                }
              }
            stage('Integration test') { 
                steps {
                echo 'Hello integration test'
            }
            }
            }
        }
      stage('deploy') {
            steps {
                echo 'Hello deploy'
            }
        }
    }
}
