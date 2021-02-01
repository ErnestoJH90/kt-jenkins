pipeline{
	agent any
	stages{
	stage('ejecutando en el Segunda'){
		steps{
			bat'ip addr show'
		}
	}
	stage('ejecutando en el agente'){
		agent{
			label 'windows'
		}
		steps{
			bat 'ip addr show'
		}
	}
	stage('solo ejecutar en tercera'){
		when{
		    expression { env.BRANCH_NAME == "Tercera"}
		}
		steps{
			bat'cat filecillo'
		}
	}
		
	}
}