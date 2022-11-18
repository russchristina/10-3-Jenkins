pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo 'Building after webhook added...'
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
		sh 'export JENKINS_NODE_COOKIE=dontKillMe'
                sh 'java -jar ./target/*.jar'
            }
        }
    }
}
