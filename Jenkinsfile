pipeline {
    agent any
    stages {
        stage('Deploy to dev') {
           steps {
                echo " %BRANCH_NAME% Branch Dev"
            }
        }
    
        stage('Deploy to test') {
           steps {
               echo " %BRANCH_NAME% Branch Test"
            }
        }

        stage('Deploy to staging') {
           steps {
                echo " %BRANCH_NAME% Branch Staging"
            }
        }


        stage('Deploy to prod') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps {
                echo "Deploying."
            }
        }
    }
}
