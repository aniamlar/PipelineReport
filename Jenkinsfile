pipeline {
   agent { label 'master' }
   stages {
       stage('before') {
           steps {
               println("before")
           }
       }
       stage('parallel run') {
           parallel {
               stage('Windows Info.') {
                   steps {
                       bat 'D:\\jenkins_script\\run_build_windows.bat'
                   }
               }
               stage('DAPC Apex - Air Permit Search') {
                   steps {
                       bat 'D:\\jenkins_script\\run_apex.bat'
                   }
               }
               stage('eBiz Disposal Report Submission') {
                   steps {
                       bat 'D:\\jenkins_script\\run_ebiz_disposal.bat'
                   }
               }
              
              
           }
       }
       stage('after') {
           steps {
               println("after")
           }
       }
   }
}
