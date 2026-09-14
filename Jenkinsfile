pipeline{
    agent any

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
                bat 'set CYPRESS_CACHE_FOLDER=%WORKSPACE%\\.cypress_cache && npx cypress install && npm test'
            }
        }
    }
}