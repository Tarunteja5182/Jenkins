pipeline{
    agent {
        node{
            label 'ROBOSHOP'
        }
    }
    environment{
        learning="devops"
    }
    stages{
        stage(Testing){
            steps{
              script{
                sh """
                  echo "Application is in testing phase"
                  echo "I am learning ${learning}"
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
            post{
            always{
                echo "I will run everytime this pipeline runs"
            }
            success{
               echo "I run only for a sucesfull pipeline"
            }
            failure{
               echo "I run only for a failure pipeline"
            }
        }
}