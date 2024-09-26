pipeline {
    agent any
    
    environment {
        name = 'Ashik'
    }
    parameters {
        string(name: 'person', defaultValue: 'Ashik Ahammad', description: 'Who am I?')
    }
    
    stages {
        stage('Hello') {
            steps {
                sh 'date'
            }
        }
        stage('Hola') {
            steps {
                echo 'Boogeyman!'
            }
        }
        stage('Env Var') {
            steps {
                sh 'echo "${BUILD_ID}"  '
                sh 'echo "${name}"  '
            }
        }
        stage('parameters') {
            steps {
                sh 'echo "${BUILD_ID}"  '
                sh 'echo "${name}"  '
                sh 'echo "${person}"  '
            }
        }
        stage('Continue ?') {
            input {
                message "Should we continue?"
                ok "Yes we should!"
            }
            steps {
                echo 'Deploy!'
            }
        }
        }
        stage('Deploy on Production') {
            steps {
                echo 'Boogeyman!'
            }
        }
    }
}
