//pipeline {
  //  agent any
//     stages {
//         stage('Execute ls command') {
//             steps {
//                 script {
//                     bat 'execute_ls.bat'
//                 }
//             }
//         }
//     }
// }
pipeline {
    agent any

    stages {
        stage('Clone Repositories') {
            steps {
                // Clone the repository with the batch script
                git branch: 'master', url: 'https://github.com/Hadeer-Adel729/CloudTask.git'


                // Clone the repository with the files you want to list
                git branch: 'main', url: 'https://github.com/Hadeer-Adel729/CmakeList-OpenCV.git'

            }
        }
        
        stage('Execute dir command') {
            steps {
                script {
                    // Run the batch script from the first repo
                    bat 'CloudTask\\execute_ls.bat'
                }
            }
        }
    }
}
