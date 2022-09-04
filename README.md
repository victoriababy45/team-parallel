pipeline {
    agent any
    stages {
        stage('parallel-level') {
            parallel {
                stage('sub-job1') {
                     steps{
                      echo "sub-job1 task" 
                     }
                }
                stage('sub-job2') {
                	steps{
                        echo "sub-job2 task"	       	
                	}
                      
                }
            }
        }
        stage ('user check'){
            steps{
                sh 'cat /etc/passwd | grep jenkin'

            }
            

                    
         }          

    }
}