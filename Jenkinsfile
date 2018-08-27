pipeline{
	agent any
	stages{
		stage('Compile Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					bat 'mvn clean compile'
				}
			}
		}
		
		stage('Code Review Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					bat 'mvn -P metrics pmd:pmd'
				}
			}
		}
		
		stage('Test Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					bat 'mvn test'
				}
			}
		}
	}
}
