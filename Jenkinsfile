
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
                    zip archive : true, dir : 'https://github.com/ShreyaAdkar/JenkinsDemo', glob : '', zipFile : 'Output.zip'
                } 
            }
        }
    }
}
