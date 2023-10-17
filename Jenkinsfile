pipeline {
    agent any
    tools { 
        maven 'M1' 
        
    }
    stages{
        stage("Checkout"){
            steps {
                echo "Checkout"
                git url:"https://github.com/sachinjangramp/SpringPetClinic.git", branch:"main"
            }
        }
        stage("Compile"){
            steps{
                sh "mvn compile"
            }
        }
        stage("Test"){
            steps{
                sh "mvn test"
            }
        }
    }
}
