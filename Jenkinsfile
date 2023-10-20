pipeline {
    agent any
    tools { 
        maven 'M1' 
        
    }
    stages{
        stage("Checkout"){
            steps {
                echo "Checkout"
                git url:'https://github.com/Piyushjais25/SpringPetClinic.git', branch:'main'
            }
       stage('validate') {
            steps {
                echo 'Validating the Maven Project'
                sh 'mvn validate'
            }
        }
        stage('clean') {
            steps {
                echo 'Cleaning the Maven Project'
                sh 'mvn clean'
            }
        }
        stage('compile') {
            steps {
                echo 'Compiling the Maven Project'
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                echo 'Testing the Maven Project'
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                echo 'Packaging the Maven Project'
                sh 'mvn package'
            }
        }
        stage('verify') {
            steps {
                echo 'Verifying the Maven Project'
                sh 'mvn verify'
            }
        }
        stage('install') {
            steps {
                echo 'Installing the Maven Project'
                sh 'mvn install'
            }
        }
        stage('executing generate jar') {
            steps {
                echo 'Executing the generate jar file'
                sh 'java -jar ./target/Sum.jar 10 25 30 55 67 89'
            }
        }
    }
}
