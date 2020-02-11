pipeline {
    agent any

    stages {
        stage('Upload to AWS') {
            steps {
                s3Upload(file:'index.html', bucket:'titan-jenkins', path:'index.html')
                  sh 'echo "Hello World"'
                  sh '''
                      echo "Multiline shell steps works too"
                      ls -lah
                  '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
    }
}
