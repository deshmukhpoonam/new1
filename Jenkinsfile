

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
	 sh "docker run -itdp 82:80 --name con-1 ubuntu 18.04 bash"
	 sh "cp -r /mnt/newhttpd/index.html con-1:/user/local/apache2/htdocs"
	}
  
  }
}

}
