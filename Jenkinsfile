pipeline {
    agent any 
    tools {
        maven 'maven'
    }
    stages {
        stage ('Checkout SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/nkjohn7/nk1.git'    
            }
        }
        stage ('Build') {
            steps {
                sh "mvn clean package"    
            }
            }
        stage ('Deploy') {
            steps {
                sh "scp -o StrictHostKeyChecking=no -i ~/mumbai.pem target/nk1.war ec2-user@172.31.47.204:/opt/tomcaat/webapps"    
            }
            }
        }
    }
