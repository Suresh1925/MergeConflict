pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main'], [name: '*/jerry'], [name: '*/ram'], [name: '*/suresh']], extensions: [], userRemoteConfigs: [[credentialsId: 'd70990d8-cc35-4ac6-be64-71426ed48650', url: 'https://github.com/Suresh1925/MergeConflict.git']])
            }
        }

        stage('Build') {
            steps {
              bat 'Test.txt'
            }
        }        
    }
}
