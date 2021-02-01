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
			label 'Docker'
		}
		steps{
			sh 'ip addr show'
		}
	}
	stage('solo ejecutar en tercera'){
		when{
		    expression { env.BRANCH_NAME == "Tercera"}
		}
		steps{
			sh 'cat filecillo'
		}
	}
		
	}
}