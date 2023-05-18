pipeline {
    agent any

    stages {
        stage('Checkout git') {
            steps {
                sh """mvn -version""";
                sh """git --version""";
                echo 'Pulling...';
                //git branch :'master',url:'https://github.com/Yassine-Azougagh/ProjetJEE.git';
                git clone 'https://github.com/Yassine-Azougagh/ProjetJEE.git';
            }
        }
    }
}
