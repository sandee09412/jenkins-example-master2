pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
              
                   'mvn clean compile'
              
            }
        }

        stage ('Testing Stage') {

            steps {
               
                    mvn test
               
            }
        }


        stage ('Deployment Stage') {
            steps {
               
                    mvn deploy
               
            }
        }
    }
}