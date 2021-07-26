pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q Sudoku-"
                bat "git clone https://github.com/kimpetertanui/Sudoku-.git"
                bat "mvn clean -f Sudoku-"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Sudoku-"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Sudoku-"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Sudoku-"
            }
        }
    }
}
