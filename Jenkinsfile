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
post {
    success {
        echo 'Testes concluídos com sucesso!'
    }
    failure {
        echo 'Testes falharam!'
    }
}