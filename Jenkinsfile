pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalação e Testes') {
            steps {
                echo 'Configurando cache local e executando...'
                withEnv(["CYPRESS_CACHE_FOLDER=${env.WORKSPACE}/node_modules/.cache/cypress"]) {
                    bat 'npm install && npx cypress install && npx cypress run --browser chrome'
                }
            }
        }
    }
}