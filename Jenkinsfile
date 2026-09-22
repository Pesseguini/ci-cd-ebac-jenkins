pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Executar Testes') {
            parallel {
                stage('Testes no Chrome') {
                    steps {
                        bat 'npm run test-chrome'
                    }
                }
                stage('Testes no Electron') {
                    steps {
                        bat 'npm run test-electron'
                    }
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
}