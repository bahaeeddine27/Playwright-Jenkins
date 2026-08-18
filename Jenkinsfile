pipeline{
    agent{
        docker{
            image 'mcr.microsoft.com/playwright:v1.62.1-jammy'
            args '-u root --entrypoint='
        }
    }
    stages{
        stage('Installation des dependences'){
            steps{
                sh 'npm install'
            }
        }
        stage('Lancement de tests'){
            steps{
                sh 'npx playwright test'
            }
        }
    }
}