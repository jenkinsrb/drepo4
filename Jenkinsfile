pipeline {
    agent any
	parameters {
		booleanParam defaultValue: true, name: 'skip_test'
		}

    stages {
        stage('build') {
            steps {
                echo 'Hello build'
            }
        }
        stage('test') {
			when {expression {params.skip_test != true}}
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
