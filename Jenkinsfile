pipeline{
   agent any
   stages{
   	stage('Stage 1'){
		steps{
		     git 'https://github.com/spring-projects/spring-petclinic'
		     dir ('spring-petclinic') {
    sh 'pwd'
}
withMaven() {

   sh "./mvnw package"
}
		}
	}
   }
}
