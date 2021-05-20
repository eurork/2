pipeline {
    agent any;
    options {
        copyArtifactPermission('deploy');
    }
    stages{
      stage('install') {
        steps {
          sh 'echo "rozpoczynam instalacje . . ."'
          sh 'sleep 1'
          copyArtifacts filter: 'test.zip', fingerprintArtifacts: true, projectName: 'build'
          unzip zipFile: 'test.zip', dir: '.'
          sh 'bash ./plik.sh'
          sh 'ls -al'
          sh 'echo "Instalacja zakonczona prawidlowo."'
        }
      }
    }
}