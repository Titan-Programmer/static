pipeline {
    agent any
    
    stages {
        stage('Upload to AWS.') {
            steps {
                withAWS(credentials:'jenkins') {
                    echo 'Uploading file'
                    s3Upload(file:'index.txt', bucket:'titan-jenkins', path:'index.html')
                }                
            }
        }        
    }
}
