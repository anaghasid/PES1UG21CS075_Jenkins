pipeline{
    agent any
    stages{
        stage('build'){
            steps {
                build 'PES1UG21CS075-1'
                sh 'g++ main2.cpp -o output'
            }

        }
        stage('test'){
            steps{
                sh './output'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
            failure{
                error 'pipeline failed'
            }
    }
}