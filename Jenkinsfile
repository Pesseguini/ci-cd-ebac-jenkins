pipeline{
    agent any

    environment {
        CYPRESS_CACHE_FOLDER = "${env.WORKSPACE}/.cypress_cache"
    }

    tools {
        nodejs 'nodejs'
    }

    stages{
        stage('Instalação de dependências'){
            steps{
                echo 'Instalando pacotes do Node.js...'
                bat 'npm install'
            }
        }

        stage('Execução dos testes'){
            steps{
                echo 'Executando os testes com Cypress...'
                bat 'npx cypress install && npm test'
            }
        }
    }
}