
node (label: 'slaves') {
 
   def app

   stage('Clone repository'){
    
      git url: 'https://github.com/vinaymamidala/Login_Docker_alphine.git',branch: 'master'

  }
  
   stage("Build image"){
    
   app = docker.build("vinaymamidala/login_docker_pipeline_automations:${env.BUILD_NUMBER}")
    
 }
}
