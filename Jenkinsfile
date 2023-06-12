pipeline { 
    agent {label 'yytest'}
    stages { 
        stage('Build') { 
            steps { 
                bat 'mkdir  test' 
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
    }
