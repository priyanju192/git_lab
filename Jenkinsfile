pipeline {
    agent any
    stages {     
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
                    echo "hello master"
                }
            }

            stage("dev task") {
                when {
                    branch 'dev'
                }
                steps {
                    sh 'ls'
                    echo "hello dev"
                }
            }
            stage("test task") {
                when {
                    branch 'test'
                }
                steps {
                    sh 'ls'
                    echo "hello test"
                }
            }
    }
}
