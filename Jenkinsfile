pipeline{
   agent {
           label {
		   
		          label "built-in"
				  customWorkspace "/mnt/project"
		         }
	      }
		 stages {
		    stage ("deploy html application"){
			
			    steps {
				  sh "service httpd restart"
				  sh "cp -r /mnt/project/index.html  /var/www/html"
				  sh "chmod -R 777 /mnt"
				      }
			    }
			}
	}
