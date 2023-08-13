pipeline {
 agent any

stages{
  stage('Checkout') {
    steps {
     
	 checkout(scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-user', url: 'https://github.com/JeelanBasha27/maven-deploy-project.git']])
    }
  }
  
   }
   stage('Validate'){
	steps {
	sh 'mvn validate'
	 }	  
   }
  
  }
