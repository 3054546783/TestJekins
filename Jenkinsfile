pipeline { 
    agent {label 'yytest'}
    stages { 
            stage('Test') { 
                steps { 
                    echo 'Testing..' 
                } 
            } 
            stage('Deploy') { 
                steps { 
                    echo 'Deploying....' 
                } 
            }
         stage('run-dryrun') {
            steps {
                echo 'run dryrun.'
				bat 'robot -d ./results test.robot'
            }
        }
        }
     post {
            always {
                archiveArtifacts artifacts: 'results/*.*', fingerprint: true
            }
        }
}

