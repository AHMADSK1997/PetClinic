pipeline{
   agent {label 'slave for HW2' }
   tools{
   	maven 'MAVEN'
   }
   stages{
   	stage('clone the code'){
		steps{
		     git branch: 'slave for HW2', url: 'https://github.com/spring-projects/spring-petclinic.git'
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
		     sh './mvnw package'
		}
	 }
   }
}
