pipeline{
	agent any
	withEnv(["JAVA_HOME=${ tool 'jdk1.8.0_141' }", "PATH+MAVEN=${tool 'MAVEN'}/bin:${env.JAVA_HOME}/bin"]) {
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
}
