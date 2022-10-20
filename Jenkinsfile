pipeline {
    agent any 
    
    tools {
        jdk 'myjava'
        maven 'mymaven'
    }
    
    stages {
        stage('Clonerepo') {
            steps {
                git 'https://github.com/gill209/DevOps-code.git'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage(CodeReview) {
            steps {
                sh 'mvn pmd:pmd'
            }
        }
        stage(UnitTesting){
            steps {
                sh 'mvn test'
            }
        }
        
    }
}
