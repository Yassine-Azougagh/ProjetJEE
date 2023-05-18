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
                 workdir ./src ;
                 build -t yassineazougagh/mainApp:1.0.0 . ;
             }
        },
          stage('Deploying image'){
             steps{
                 #docker-compose.yml
                 version: '2'
                 services:
                     mainApp:
                        image: yassineazougagh/mainApp:1.0.0
                        ports:
                        -   "9000:9000"
                     mysql:
                         image: mysql
                        ports:
                        -   "3306:3306";
                 docker compose up ;
             }
        }   
    }
}
