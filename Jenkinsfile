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
                        bat 'npx cypress run --browser chrome'
                    }
                }

                stage('Testes no Electron') {
                    steps {
                        bat 'npx cypress run --browser electron'
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