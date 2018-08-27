pipeline{
	agent any
	tools { 
        	maven 'MAVEN' 
        	jdk 'jdk1.8.0_141' 
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
