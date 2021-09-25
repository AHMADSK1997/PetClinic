# PetClinic
HW2 (Jenkins) Spring PetClinic Sample Application

1) First we create a Github Repository with  name PetClinic

2) Create a Jenkins Pipeline Job:

 - click on New Item (an Item is a job). 
 
 - Name your "PetClinic" and select the Pipeline type. Click ok.
 
 - Configure Pipeline Job, choose in pipeline->Definition "pipeline script from SCM" and enter the Repository URL of the Github "https://github.com/AHMADSK1997/PetClinic", choose  Script Path "Jenkinsfile", and select Apply and Save
 

3) After that we write the code in Jenkinsfile on github.

  - To make the code running on slave we use : agent {label 'slave'}

  - To clone the PetClinic GitHub repository: git url: 'https://github.com/spring-projects/spring-petclinic.git'

  - To enther to spring-petclinic directory :  dir ('spring-petclinic')

  - To install the packages : script {'./mvnw package'}

4) We run the Application on the Jenkins by clicking on Build Now
