pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalação e Testes') {
            steps {
                echo 'Instalando dependências, baixando o Cypress e rodando os testes...'
                bat 'npm install && npx cypress install && npx cypress run --browser chrome'
            }
        }
    }
}