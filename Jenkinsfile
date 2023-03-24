

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
	 sh "docker run -itdp 83:80 --name con-11 httpd"
	 sh "cp -r /mnt/newhttpd/index.html con-11:/user/local/apache2/htdocs"
	}
  
  }
}

}
