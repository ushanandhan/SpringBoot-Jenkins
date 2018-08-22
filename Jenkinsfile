pipeline{
	agent any
	
	stages{
		stage('Compile Stage'){
		
			steps{
				withMaven(maven:'MAVEN-3.0.5'){
					sh 'mvn clean compile'
				}
			}
		}
		
		stage('Code Review Stage'){
		
			steps{
				withMaven(maven:'MAVEN-3.0.5'){
					sh 'mvn -P metrics pmd:pmd'
				}
			}
		}
		
		stage('Test Stage'){
		
			steps{
				withMaven(maven:'MAVEN-3.0.5'){
					sh 'mvn test'
				}
			}
		}
	}
}