pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo 'Building...'
                sh 'sudo sh ./mvnw clean package -DskipTests'
            }
        }

        stage('Test'){
            steps{
                echo 'Running tests...'
            }
        }

        stage('Deploy'){
            steps{
                echo 'Deploying app...'
                sh 'java -jar ./target/*.jar'
            }
        }
    }
}