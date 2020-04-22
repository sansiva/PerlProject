pipeline {
    agent any
    stages {
        
         stage('Example Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying master'
            }
        }
        
        stage('Deploy to dev') {
           steps {
               echo " ${env.BRANCH_NAME} Branch Dev"
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
