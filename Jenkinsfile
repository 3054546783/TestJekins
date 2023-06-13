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
     post{
           always {
                robot disableArchiveOutput: false, outputFileName: 'dryrun.xml', outputPath: 'outputdir', passThreshold: 100.0, unstableThreshold: 99.0
           }
           success {
                cleanWs()
            }
       }   
}

