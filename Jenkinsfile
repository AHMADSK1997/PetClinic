pipeline{
   agent {label 'slave' }
   stages{
   	stage('clone the code'){
		steps{
		     git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
		     }
	}
	
	 stage('Build the code'){
	 	steps{
		     sh './mvnw package'
		}
	 }
	   stage('Run the App'){
		   steps{
			   sh 'JENKINKS_NODE_COOKIE=do_not_kill nohup java -jar target/*.jar &'
		   }
	   }
   }
}
