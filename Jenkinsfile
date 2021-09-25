pipeline{
   agent any
   stages{
   	stage('clone the code'){
		steps{
		     git 'https://github.com/spring-projects/spring-petclic.git'
		     }
	}
	stage('change dir'){
		steps{
		     dir ('spring-petclinic') {
    		     sh 'pwd'
		     }	
		 }
	 }
	 stage('maven'){
	 	steps{
		     withMaven() {
		     sh "./mvnw package"
			}
		}
	
	}
   }
}
