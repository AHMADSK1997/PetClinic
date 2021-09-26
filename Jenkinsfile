pipeline{
   agent {label 'slave' }
   tools{
   	maven 'MAVEN'
   }
   stages{
   	stage('clone the code'){
		steps{
		     git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
		     }
	}
	
	 stage('maven'){
	 	steps{
		     sh './mvnw package'
		}
	 }
   }
}
