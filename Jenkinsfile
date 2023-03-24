

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
	 sh "docker run -itdp 86:80 --name con-16 httpd"
	 sh "cp /mnt/newhttpd/index.html con-16:/usr/local/apache2/htdocs"
	 sh "chmod -R 777 /mnt/newhttpd/index.html"
	}
  
  }
}

}
