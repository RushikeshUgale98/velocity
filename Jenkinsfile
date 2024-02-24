pipeline {

	agent {
		label "built-in"
	}

	stages {
	
		stage ('install-httpd'){
		
			steps {
					sh "sudo yum install httpd -y"
					
			}	
		}
		
		stage ('start-httpd'){
			
			steps {
					sh "sudo service httpd start"
			}
		
		}
		
		stage ('deploy-index') {
			
			steps {
						sh "sudo echo 'hello' >> /var/www/html/index.html"
						sh "sudo chmod 777 /var/www/html/index.html"
			}
		
		}
	}

}
