pipeline {
    agent any
    
    stages {
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
