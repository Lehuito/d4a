pipeline{
        agent any
        stages{
                stage("Initial Setup"){
                        steps{
                                sh "echo Starting..."
                        }
                }
                stage("Checking Docker"){
                        steps{
                                sh "sudo docker ps"
                        }
                }
                stage("Build Docker"){
                        steps{
				sh "sudo docker image rm stage3"
				sh "sudo docker build --tag=stage3 ."
			}
		}
		stage("Deploy Container"){
			steps{
				sh "sudo docker-compose down"
				sh "sudo docker-compose up -d"
			}
		}
        }
}
