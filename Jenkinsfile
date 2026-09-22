pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalar Dependências') {
            steps {
                bat 'npm install'
                bat 'npx cypress install'
            }
        }

        stage('Executar Testes') {
            parallel {
                stage('Testes da suite-1') {
                    steps {
                        bat 'npm run teste-suite-1'
                    }
                }
                stage('Testes da suite-2') {
                    steps {
                        bat 'npm run teste-suite-2'
                    }
                }
                stage('Testes da suite-3') {
                    steps {
                        bat 'npm run teste-suite-3'
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