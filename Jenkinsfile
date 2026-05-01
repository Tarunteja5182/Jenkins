pipeline{
    agent {
        node{
            label 'ROBOSHOP'
        }
    }
    environment{
        learning="devops"
    }
        parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage(Testing){
            steps{
              script{
                sh """
                  echo "Application is in testing phase"
                  echo "I am learning ${learning}"
                  echo "Hello ${params.PERSON}"
                  echo "Biography: ${params.BIOGRAPHY}"
                  echo "Toggle: ${params.TOGGLE}"
                  echo "Choice: ${params.CHOICE}"
                  echo "Password: ${params.PASSWORD}"
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