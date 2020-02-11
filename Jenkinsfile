pipeline {
    agent any

    stages {
        stage('Upload to AWS') {
            sh 'attempting to upload'
            s3Upload profileName: 'example', entries [
                [
                    bucket              : 'titan-jenkins',
                    selectedRegion      : 'eu-west-2',
                    sourceFile          : 'index.html',
                    managedArtifacts    : true,
                ]
            ]
            steps {
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
