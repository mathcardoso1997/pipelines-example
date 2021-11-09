pipeline {
    agent any
    
    environment {
        NOME = 'Matheus'
        SOBRENOME = 'Cardoso'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'echo $NOME'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'echo $SOBRENOME'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        
        stage('Reports') {
            steps {
                echo 'Criando reports...'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    
    post {
        always {
            echo 'Sempre serei executado'
        }
        
        success {
            echo 'Serei executado apenas quando a pipeline der sucesso'
        }
        
        failure {
            echo 'Serei executado apenas quando a pipeline der erro'
        }
        
        unstable {
            echo 'Serei executado apenas quando a pipeline encerrar instavel'
        }
    }
    
}
