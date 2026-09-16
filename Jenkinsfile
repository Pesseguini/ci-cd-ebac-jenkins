pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalação de dependências') {
            steps {
                echo 'Instalando pacotes e binário do Cypress localmente...'
                bat 'npm install && npx cypress verify'
            }
        }

        stage('Execução dos testes') {
            steps {
                echo 'Executando os testes com Cypress...'
                bat 'npx cypress run --browser chrome'
            }
        }
    }
}