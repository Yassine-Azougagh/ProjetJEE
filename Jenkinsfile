pipeline {
    agent any

    stages {
        stage('Checkout git') {
            steps {
                
                sh """mvn -version""";
                sh """git --version""";
                echo 'Pulling...';
                git branch :'master',url:'https://github.com/Yassine-Azougagh/ProjetJEE.git';
                sh """date""";
                
            }},
         stage('Builsing image'){
             steps{
                 from openjdk:8
                 workdir ./src
                 
             }
        }
    }
}
