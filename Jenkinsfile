pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                withAWS(credentials:'jenkins') {
                    echo 'Building..'
                }
                
            }
        }        
    }
}
