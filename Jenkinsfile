pipeline {
    agent any
    stages {
        stage ('Deploy') {
            steps {
                echo "Deploy"
                sh 'mkdir archive'
                sh 'echo test > archive/test.txt'
                zip zipFile: 'Output.zip', archive: false, dir: 'archive'
                archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
    }    
    }
