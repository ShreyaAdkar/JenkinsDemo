
pipeline {
    agent any
    stages {
        stage ('push artifact') {
            steps {
                sh 'mkdir archive'
                sh 'echo Output > archive/Output.txt'
                zip zipFile : 'Output.zip', dir : 'https://github.com/ShreyaAdkar/JenkinsDemo/tree/main/Output'
                archiveArtifacts artifacts : 'Output.zip', fingerprint : true
            }
        }
    }
    }
