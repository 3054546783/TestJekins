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
        }
     post {
            always {
                archiveArtifacts artifacts: 'results/*.*', fingerprint: true
            }
        }
}

