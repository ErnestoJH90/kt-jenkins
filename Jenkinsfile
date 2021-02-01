pipeline{
	agent any
	stages{
	stage('ejecutando en el master'){
		steps{
			bat 'ipconfig '
		}
	}
	stage('ejecutando en el agente'){
		agent{
			label 'docker'
		}
		steps{
			sh 'ip addr show'
		}
	}
    
	}
}
