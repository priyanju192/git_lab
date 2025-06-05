pipeline {
    agent any
    stages {
                        
            stage("Checkout Code") {
                steps {
                checkout scm
                }
            }
         
            stage('task') {
                steps {
                     sh "ls"
                }
            }

            stage("master task") {
                when {
                    not {
                        anyof {
                            branch 'dev';
                            branch 'test'
                        }
                    }
                }
                steps {
                    sh 'ls'
                    sh ' echo "hello master" '
                }
            }

            stage("dev task") {
                when {
                    branch 'dev'
                }
                steps {
                    sh 'ls'
                    sh ' echo "hello dev" '
                }
            }
            stage("test task") {
                when {
                    branch 'test'
                }
                steps {
                    sh 'ls'
                    sh ' echo "hello test" '
                }
            }
    }
}