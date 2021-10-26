pipeline {
    agent any
    stages {
        stage ('Deploy') {
            steps {
                echo "Deploy"
                //sh 'mkdir archive'
                //sh 'echo test > archive/test.txt'
                zipFile : 'Output'  ,dir :''
                //archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
    }    
    }
