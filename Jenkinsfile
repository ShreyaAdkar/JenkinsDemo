pipeline {
    agent any
    stages {
        stage ('Deploy') {
            steps {
                echo "Deploy"
                //sh 'mkdir archive'
                //sh 'echo test > archive/test.txt'
                zip zipFile : 'Output.zip' , archive : true ,url :'https://github.com/ShreyaAdkar/JenkinsDemo/tree/main/Output'
                //archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
    }    
    }
