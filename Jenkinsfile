pipeline {
	agent any
	//agent { docker { image 'maven:3.8.5' } }
	//agent { docker { image 'node:13.8' } }
	environment {
		dockerHome = tool 'docker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
       stage('Build') {
		   steps {
			   sh 'mvn --version'
			   sh 'docker version'
		     echo "Build"
			 echo "PATH - $PATH"
			 echo "BULD_NUMBER - $env.BULD_NUMBER"
			 echo "BULD_ID - $env.BULD_ID"
			 echo "JOB_NAME - $env.JOB_NAME"
			 echo "BULD_TAG - $env.BULD_TAG"
			 echo "BULD_URL - $env.BULD_URL"
	        }
	   }	
	   stage('Test') {
		   steps {
		     echo "Test"
	       }
	   }   
	   stage('Integration Test') {
		   steps {
		     echo "Test"
            }
       }
	}
	
	post {
		always {
			echo 'I m awesome.I run always'
		}
		success {
		   echo 'I run when you are successful'	
		}
		failure {
		   echo 'I run when you are fail'	
		}  
	}
}	


	
