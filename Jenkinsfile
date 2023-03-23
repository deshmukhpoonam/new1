pipeline{
    ageny any
  stages{
    stage ("deploy on docker container"){
     steps{
         
         sh "docker run -itdp 80:80 --name server httpd"
         sh "cp /root/.jenkins/workspace/index.html  /user/local/apache2/htdocs"
          }
     }
}

}
