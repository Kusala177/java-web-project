pipeline
    agents any
    stages{
        stage('build'){
            steps{
                sh "mvn clean package"
            }
        }
        stage('deploy'){
            steps{
                deploy adapters: [tomcat7(credentialsId: '2d76a3d8-e61c-4e9e-af5b-61738718d63f', 
                path: '', 
                url: 'http://ec2-52-15-53-114.us-east-2.compute.amazonaws.com:8080/')], 
                contextPath: 'javawebapp', 
                war: '**/java-web-project.war'
            }
        }
    }
        
