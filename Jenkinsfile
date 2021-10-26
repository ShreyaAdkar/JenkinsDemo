
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
                    zip archive : true, dir : '', glob : '', zipFile : 'Output.zip'
                } 
            }
        }
    }
}
rtServer (
    id: 'demo1',
    url: 'http://localhost:8082//artufactory//demo1',
    // If you're using username and password:
    username: 'admin',
    password: 'password@123',
    // If you're using Credentials ID:
    //credentialsId: 'ccrreeddeennttiiaall',
    // If Jenkins is configured to use an http proxy, you can bypass the proxy when using this Artifactory server:
    bypassProxy: true,
    // Configure the connection timeout (in seconds).
    // The default value (if not configured) is 300 seconds:
    timeout: 300
)

