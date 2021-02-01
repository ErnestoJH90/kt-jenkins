pipeline{
	agent any
	stages{
	stage('ejecutando en el Segunda'){
		steps{
			sh 'ip addr show'
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