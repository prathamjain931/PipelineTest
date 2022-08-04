pipeline{
	agent any
	tools{
		maven "Maven3.8.6"
	}
	
	stages{
		stage('SCM CheckOut'){
			steps{
				git 'Https://github.com/prathamjain931/PipelineTest'
			}
		}
		stage('Compile-Package'){
			steps{
				sh "mvn -version"
				sh "mvn clean install"
				sh "mvn package"
			}
		}
	}
	
	post{
		always{
			cleanWS()
		}
	}
}

		
