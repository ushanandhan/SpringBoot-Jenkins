pipeline{
	agent any
	
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