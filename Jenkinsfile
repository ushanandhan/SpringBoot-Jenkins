pipeline{
	agent any
	tools { 
        	jdk 'Java8'
			maven 'Maven_3.5.4'
    }
	stages{
		stage('Compile Stage'){
			steps{
					sh 'mvn clean compile'
			}
		}
		
		stage('Test Stage'){
			steps{
					sh 'mvn test'
			}
		}
	}
}
