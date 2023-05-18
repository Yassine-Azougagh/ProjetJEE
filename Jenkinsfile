pipeline {
    agent any

    stages {
        stage('Checkout git') {
            steps {
                sh """mvn -version""";
                echo 'Pulling...';
                git branch: 'main',
                url:'https://github.com/Yassine-Azougagh/ProjetJEE.git'
            }
        }
    }
}
