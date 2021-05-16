

node (label: 'slaves') {

//def groovyHome = tool 'groovy-default'
  
   def app

   stage('Clone repository'){
    
      git url: 'https://github.com/vinaymamidala/Login_Docker_alphine.git',branch: 'master'

  }
  
   stage("Build image"){
    
   app = docker.build("vinaymamidala/login_docker_pipeline_automations:${env.BUILD_NUMBER}")
    
 }
  
  stage('Test image'){
    app.inside {
        sh 'echo "Test Passed"'
    }
   }
  
  stage('Push image'){
    docker.withRegistry('https://registry.hub.docker.com', 'DockerHub_login') {
      app.push()
    }
  }
}
