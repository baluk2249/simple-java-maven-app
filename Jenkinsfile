pipeline{
    agent { docker{
        image 'maven:3.9.2-amazoncorretto-17'
    } }
    stages {
        stage('Checkout'){
        steps {
            git 'https://github.com/baluk2249/simple-java-maven-app.git'
            
        }
        }
        stage('Build')
        {
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    stage('Package'){
        steps{
            sh 'mvn package'
        }
    }
    stage('Deliver'){
        steps {
            sh './jenkins/scripts/deliver.sh'
        }
    }

    }
}