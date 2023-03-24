
## index.html deploy on docker container without volume
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
	 sh "docker run ubuntu 18.04 -itdp 82:80 --name con-1 "
	 sh "cp -r /mnt/newhttpd/index.html /user/local/apache2/htdocs"
	}
  
  }
}

}
