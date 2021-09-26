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
	stage('shange dir'){
		steps{
		     dir ('spring-petclinic') {
    		     sh 'pwd'
		     }	
		 }
	 }
	 stage('maven'){
	 	steps{
		     script {'./mvnw package'}
		}
	 }
   }
}
