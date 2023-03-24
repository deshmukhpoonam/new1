

pipeline {
  agent {
   label {
      label "built-in"
	  customWorkspace "/mnt/newhttpd"
        }
	}

 stages {
  stage ("deploy-on-doc-con"){
    steps {
	 sh "systemctl start docker"
	 sh "docker run -itdp 87:80 --name con-17 httpd"
	 sh "cp /mnt/newhttpd/index.html con-17:/usr/local/apache2/htdocs"
	 sh "chmod -R 777 /mnt/newhttpd/index.html"
	}
  
  }
}

}
