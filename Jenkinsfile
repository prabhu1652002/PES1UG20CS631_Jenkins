pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS631.cpp'
                sh 'g++ -o PES1UG20CS631 PES1UG20CS631.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS631'
                echo 'Test stage executed successfully'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed Successfully'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
