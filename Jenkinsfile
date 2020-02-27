pipeline{
	agent any
	tools { 
        	jdk 'Java8' 
    	}
	stages{
		stage('Compile Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					sh 'mvn clean compile'
				}
			}
		}
		
		stage('Code Review Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					sh 'mvn -P metrics pmd:pmd'
				}
			}
		}
		
		stage('Test Stage'){
		
			steps{
				withMaven(maven:'MAVEN'){
					sh 'mvn test'
				}
			}
		}
	}
}
