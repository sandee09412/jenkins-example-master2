pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
		 	steps {
             mvnHome = tool 'M2_HOME' 
                bat(/"${mvnHome}\bin\mvn" clean compile/)
            }
        }

        stage ('Testing Stage') {
			 steps {
                withMaven(maven : 'maven_3_5_3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}