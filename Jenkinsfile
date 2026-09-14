pipeline{
    agent any

    stages{
        stage('Instalação de dependências'){
            steps{
                bat 'npm install'
                
            }
        }

            stages{
        stage('Execução dos testes'){
            steps{
                bat 'npm test'
                
            }
        }
    }



}}
