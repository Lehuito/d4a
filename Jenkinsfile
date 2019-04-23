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
								sh "ADD https://github.com/Lehuito/d4a/blob/master/Dockerfile /var/jenkins_home/workspace/Pipeline EDSI"
								sh "ADD https://github.com/Lehuito/d4a/blob/master/db.php /var/jenkins_home/workspace/Pipeline EDSI"
								sh "ADD https://github.com/Lehuito/d4a/blob/master/index.php /var/jenkins_home/workspace/Pipeline EDSI"
								sh "sudo docker build --tag=stage3 ."
						}
				}
				
        }
}
