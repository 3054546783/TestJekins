pipeline { 
    agent {label 'yytest'}
    stages { 
        stage('Build') { 
            steps { 
                bat 'mkdir  test2' 
                } 
            } 
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
				bat 'python.exe run.py -e not-ready --dryrun -d ./results'
            }
        }
        }
     post {
            always {
                archiveArtifacts artifacts: 'results/*.*', fingerprint: true
            }
        }
}

