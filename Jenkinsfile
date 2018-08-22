pipeline{
	agent any
	
	stages{
		stage('Compile Stage'){
		
			steps{
				sh 'mvn clean compile'
				
			}
		}
		
		stage('Code Review Stage'){
		
			steps{
				sh 'mvn -P metrics pmd:pmd'
				
			}
		}
		
		stage('Test Stage'){
		
			steps{
				sh 'mvn test'
				
			}
		}
	}
}