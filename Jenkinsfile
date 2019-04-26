pipeline{
	agent any
	stages{
		stage('Starting'){
			steps{
				sh 'echo starting...'
			}	
		}
		stage('Checking Docker'){
			steps{
			 sh 'sudo docker ps'
			}
		}
		stage('Build Image'){
			steps{
			 sh 'sudo docker build --tag=imgphpjen .'
			 sh 'sudo docker cp . imgphpjen:/var/www/html'	
			}
		}
		stage('Run Composer'){
			steps{
			sh 'sudo docker-compose up -d' 
			}
		}
	}
}
