pipeline {
  agent any
   stages {
        stage ('Deploy') {
            steps {
               echo "Deploy"
                //sh 'mkdir archive'
                //sh 'echo test > archive/test.txt'
              zip zipFile : 'Output.zip'  ,dir :''
                //archiveArtifacts artifacts: 'test.zip', fingerprint: true
            }
        }
    }    
    }
pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                sh 'mkdir archive'
                sh 'echo test > archive/Output.txt'
                zip zipFile : 'Output.zip', dir : 'https://github.com/ShreyaAdkar/JenkinsDemo/tree/main/Output'
                archiveArtifacts artifacts : 'Output.zip', fingerprint : true
            }
        }
        ...
    }
