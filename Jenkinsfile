pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalação de dependências') {
            steps {
                echo 'Instalando dependências e forçando o download do binário do Cypress...'
                bat 'npm install && npx cypress install'
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