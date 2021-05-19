pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                echo "rozpoczynam instalacje . . ."
                sleep 1
                bash ./plik.sh
                sleep 1
                ls -al
                echo "Instalacja zakończona prawidłowo."
            }
        }
    }
}
