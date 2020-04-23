pipeline {
agent any
    stages {

        stage('Checkout code') {
            steps {
                
            checkout([$class: 'GitSCM', branches: [[name: '*/dev']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'githubmvn', url: 'https://github.com/sansiva/PerlProject.git']]])
            
            }
        }
    }
}
