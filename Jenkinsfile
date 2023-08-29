// pipeline{
//     agent any
//     stages{
//         stage('Checkout'){
//             steps {
//                     checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'ad6c865f-ad1f-4aa0-8e9a-115ce91766cc', url: 'https://github.com/bdivya19/PythonDemo.git']])
//                 }
//            }
//          stage('Execute'){
//              steps{
//                 bat 'python hello.py'
//              }
//           }
//           stage('Mail'){
//             steps{
//             mail bcc: '', body: 'This is a test email😊', cc: '', from: '', replyTo: '', subject: 'Test pipeline email', to: 'bodduluridivya19@gmail.com'
//             }
//          }
//
// }

pipeline {
    agent any

    stages {
        stage('CHECKOUT') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'ad6c865f-ad1f-4aa0-8e9a-115ce91766cc', url: 'https://github.com/bdivya19/PythonDemo.git']])
            }
        }
        stage('EXECUTE'){
            steps{
                bat 'python hello.py'
            }
        }
        stage('MAIL'){
            steps{
                mail bcc: '', body: 'This is a test email😊', cc: '', from: '', replyTo: '', subject: 'Test pipeline email', to: 'bodduluridivya19@gmail.com'
            }
        }
    }
}
