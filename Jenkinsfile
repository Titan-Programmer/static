pipeline {
    agent any
    
    stages {
        stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'            
            }
        }   
        stage('Upload to AWS.') {
            steps {
                withAWS(credentials:'jenkins') {
                    echo 'Uploading file'
                    s3Upload(file:'index.html', bucket:'titan-jenkins', path:'index.html')
                }                
            }
        }        
    }
}
