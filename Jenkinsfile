pipeline {
    agent {
	  label {
	      label "built-in"
		  customWorkspace "/mnt/data"
	       }
	    }
 stages {
  stage ("deploy-on-con-vol"){
     steps {
	   sh "docker volume create vol1"
	   sh "cp /mnt/data/index.html /var/lib/docker/volumes/vol1/_data"
	   sh "docker run -itdp 89:80 -v index.html:/usr/local/apache2/htdocs --name httpd httpd"
	       }
  
        }
    }
}
