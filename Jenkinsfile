pipeline {
    agent any;
    environment {
      VERSION = '1.0'
    }
    stages{
      stage('install') {
        steps {
          sh 'echo "rozpoczynam instalacje . . ."'
          sh 'sleep 1'
          copyArtifacts filter: 'test.zip', fingerprintArtifacts: true, projectName: "build_1.0"
          unzip zipFile: 'test.zip', dir: '.'
          sh 'bash ./plik.sh'
          sh 'ls -al'
          sh 'echo "Instalacja zakonczona prawidlowo."'
        }
      }
    }
}