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
                bat 'npx cypress install --force && npx cypress run --browser chrome'
            }
        }
    }
}