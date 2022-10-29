pipeline {
	agent {
  label {
    label 'Jenkins-slave'
    retries 3
  }
}

stages{
  stage('Checkout') {
    steps {
     checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-user', url: 'https://github.com/JeelanBasha27/maven-deploy-project.git']]])
    }
  }
  stage('Validate'){
	steps{
	sh 'mvn validate'
	 }
  
   }
  }

}
