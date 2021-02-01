pipeline{
	agent any
	stages{
	stage('ejecutando en el master'){
		steps{
			bat 'ip addr show'
		}
	}
	stage('ejecutando en el agente'){
		agent{
			label 'localhost:8080'
		}
		steps{
			bat 'ip addr show'
		}
	}
		
	}
}
