pipeline{
    agent { docker{
        image 'maven:3.8.1-jdk-11'
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
    }
}