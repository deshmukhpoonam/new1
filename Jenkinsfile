
pipeline{
  agent {
    label {
	
	   label "built-in"
	   customWorkspace "/mnt/docker"
	      }
      }
	stages {
	 stage ("deploy-on-docker-container-wiout-vol"){
	    steps {
		   sh "systemctl start docker"
		   sh "docker pull ubuntu:18.04"
                   sh "docker run -itdp 81:80 --name servernew1 ubuntu:18.04"
		   sh "cp -r /mnt/docker/index.html  /mnt/docker/servernew1:/tmp" 
           		   
		    }
		}
	 
	 }
	 
   }
