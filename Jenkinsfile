pipeline{
	agent any
	tools { 
        	jdk 'Java8'
			maven 'Maven_3.5.4'
    }
	stages{
		stage('Compile Stage'){
			steps{
					bat 'mvn clean compile'
			}
		}
		
		stage('Code Review Stage'){
			steps{
					bat 'mvn -P metrics pmd:pmd'
			}
		}
		
		stage('Test Stage'){
			steps{
					bat 'mvn test'
			}
		}
	}
}
