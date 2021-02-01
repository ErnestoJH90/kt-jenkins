pipeline{
	agent any
	stages{
	stage('ejecutando en el master'){
		steps{
			sh 'ip addr show'
		}
	}
	stage('ejecutando en el agente'){
		agent{
			label 'Docker'
		}
		steps{
			sh 'ip addr show'
		}
	}

	}
}
