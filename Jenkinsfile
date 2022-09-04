pipeline{
  agent any
  stages{
    stage('actions1 and actions2'){
      parallel{
        stage('actions1'){
          steps{
            sh 'actions1'
          }
        }
        stage('actions2'){
          steps{
            sh 'actions2'
          }
        }
      }
    }
    stage('codebuild'){
    	steps{
    		sh 'echo codebuild stage'
    	}
    }
  }
}