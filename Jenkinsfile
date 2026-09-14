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
                bat 'npx cypress install'
                bat 'npm test'
            }
        }
    }
    post{
        success{
            echo 'Build e testes concluídos com sucesso!'
        }
        failure {
            echo 'Build ou testes falharam!'
        }
    }
}
