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
	   sh "docker create vol vol1"
	   sh "cp /mnt/data/index.html /var/lib/docker/volumes/vol1/_data"
	   sh "docker run -itdp 88:88 -v index.html:/usr/local/apache2/httpd"
	       }
  
        }
    }
}
