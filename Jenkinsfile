node {
    stage('Install') {
        sh 'echo "rozpoczynam instalacje . . ."'
        sh 'sleep 1'
        sh 'bash ./plik.sh'
        sh 'sleep 1'
        sh 'ls -al'
        sh 'echo "Instalacja zakonczona prawidlowo."'
    }
}

// pipeline {
//     agent any
//     stages {
//         stage('Install') {
//             steps {
//                 echo "rozpoczynam instalacje . . ."
//                 sleep 1
//                 bash ./plik.sh
//                 sleep 1
//                 ls -al
//                 echo "Instalacja zakonczona prawidlowo."
//             }
//         }
//     }
// }