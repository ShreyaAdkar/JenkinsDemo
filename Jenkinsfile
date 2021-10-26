pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
               Zip zipFile: 'Output.Zip', dir:'https://github.com/ShreyaAdkar/JenkinsDemo/tree/main/Output'
            }
        }
    }
}
//pipeline { 
    //agent any 
       // stages{ 
           // stage ('push artifact'){ 
                //steps { sh 'mkdir archive' sh  
                       // { [Pipeline] echo ZIP [Pipeline] 
                        // echo END - ZIP [Pipeline] }
