pipeline {
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/Akshiv20/java-hello-world-with-maven.git"
            }
        }
        stage("Build"){
            steps {
                dir("java-hello-world-with-maven") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                dir("java-hello-world-with-maven") {
                    sh "mvn test"
                }
            }
        }  
    }
}
