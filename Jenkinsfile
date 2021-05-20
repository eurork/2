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
          script{
            unzip zipFile: 'test.zip', dir: './archive_new'
          }
          sh 'cd archive_new'
          sh 'bash ./plik.sh'
          sh 'ls -al'
          sh 'echo "Instalacja zakonczona prawidlowo."'
        }
      }
    }
}