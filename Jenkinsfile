
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/akshay503yadav-123/my-java-tomcat-pipelineproject.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Java project...'
                sh 'mvn clean package'  // builds your project using Maven
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Tomcat...'
                sh 'cp target/*.war /path/to/tomcat/webapps/' // copy WAR to Tomcat
            }
        }
    }
}
