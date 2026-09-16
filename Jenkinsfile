pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Executar Testes') {
            steps {
                echo 'Rodando Cypress...'
                bat 'npx cypress run --browser chrome'
            }
        }
    }
}