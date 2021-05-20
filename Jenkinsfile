pipeline {
    agent any
    environment {
      VERSION = '1.0'
    }
    stages{
      stage('install') {
        steps {
          sh 'echo "rozpoczynam instalacje . . ."'
          sh 'sleep 1'
          copyArtifacts filter: 'test.zip', fingerprintArtifacts: true, projectName: "build-${VERSION}"
          unzip zipFile: 'test.zip', dir: '.'
          sh 'bash ./plik.sh'
          sh 'ls -al'
          sh 'echo "Instalacja zakonczona prawidlowo."'
        }
      }
    }
}