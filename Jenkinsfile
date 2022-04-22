pipeline {
	//agent any
	agent { docker { image 'maven:3.8.5' } }
	stages {
       stage('Build') {
		   steps {
			   sh "mvn --version"
		     echo "Build"
	        }
	   }	
	   stage('Test') {
		   steps{
		     echo "Test"
	       }
	   }   
	   stage('Integration Test') {
		   steps{
		     echo "Test"
            }
       }
	}
	
	post{
		always{
			echo 'I m awesome.I run always'
		}
		success{
		   echo 'I run when you are successful'	
		}
		failure{
		   echo 'I run when you are fail'	
		}  
	}
}	


	
