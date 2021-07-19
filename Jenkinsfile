pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				sh "docker pull khansuhaib/selenium-docker"
			}
		}
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d hub chrome"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module"
			}
		}
	}
}
