pipeline {
    agent any

    stages {
        stage ('Compile') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Test') {

            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment') {
            steps {
                withMaven(maven : 'maven_3_5_2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}