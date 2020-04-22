pipeline {
    agent any
    stages {
        
         
        
        stage('Deploy to dev') {
           steps {
               echo " ${env.BRANCH_NAME} Branch Dev"
               
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'githubmvn', url: 'https://github.com/sansiva/PerlProject.git']]])
            }
        }
    
        stage('Deploy to test') {
           steps {
               echo " ${env.BRANCH_NAME} Branch Test"
            }
        }

        stage('Deploy to staging') {
           steps {
                echo " ${env.BRANCH_NAME} Branch Staging"
            }
        }


        stage('Deploy to prod') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps {
                echo " ${env.BRANCH_NAME} Deploying Prod."
            }
        }
    }
}
