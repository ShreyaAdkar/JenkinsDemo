
pipeline {
    agent any 
    stages{
        stage('test'){
            //agent { label 'windows' }
            steps{
                //deleteDir()
                //sh 'mkdir -p archive'
                //sh 'echo Output > archive/Output.txt'
                script{
                    zip archive: false, dir: 'D:\Workspace', glob: '', zipFile: 'Output.zip'
                } 
            }
        }
    }
}
