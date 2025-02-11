pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo Version'){
            steps{
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        stage('Build'){
            steps {
                // get some code from github repository
                //git branch: 'main', url: 'https://github.com/jenkins-kk-demo/parameterized-pipeline-job-init.git'
                
                //Run Maven Package SMD
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage('Unit Test'){
            steps{
                sh "mvn test"
            }
        }
    }
}
