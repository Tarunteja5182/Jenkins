pipeline{
    agent any
    stages{
        stage(Testing){
            steps{
              script{
                sh """
                  echo "Application is in testing phase"
                """
              }
            }
        }
        stage(Building){
            steps{
                script{
                    sh """
                      echo "application is in building phase"
                    """
                }
            }
        }
        stage(Deploy){
            steps{
                script{
                    sh """
                    echo "application is deployed"
                    """
                }
            }
        }
    }
}