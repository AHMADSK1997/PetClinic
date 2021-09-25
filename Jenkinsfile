pipeline{
   agent any
   tools{
   	manen 'MAVEN'
   }
   stages{
   	stage('clone the code'){
		steps{
		     git 'https://github.com/spring-projects/spring-petclinic.git'
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
