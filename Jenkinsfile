pipeline {
    agent any
    stages{
        stage("run frontend"){
            steps{
                echo 'executing yarn...'
                nodejs('Node') {
                    sh 'yarn install'
                }
            }
        }
        stage("run backend"){
            steps{
                echo 'executing gradle...'
                withMaven() {
                    sh './maven -v'
                }
            }
        }
    }
}
