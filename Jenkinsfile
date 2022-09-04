pipeline{
  agent any
  stages{
    stage('actions1 and actions2'){
      parallel{
        stage('actions1'){
          steps{
            echo "actions1"
          }
        }
        stage('actions2'){
          steps{
            echo "actions2"
          }
        }
      }
    }
    stage('version-check'){
    	steps{
    		echo "end of parallel job"
    	}
    }
  }
}
