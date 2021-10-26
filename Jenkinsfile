pipeline {
    agent any
    stages {
        stage ('Deploy') {
            steps {
                echo "Deploy"
                //sh 'mkdir archive'
                //sh 'echo test > archive/test.txt'
                zip label : 'Output.zip'  ,url :'https://github.com/ShreyaAdkar/JenkinsDemo/tree/main/Output'
                //archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
    }    
    }
