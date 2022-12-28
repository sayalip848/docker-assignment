pipeline {
    agent {
	label {
		label 'built-in'
		customWorkspace '/mnt/docker'
  }
}
stages {
        stage ('git') {
            steps {
                git url: 'https://github.com/sayalip848/docker-assignment.git'
            }
        }       
stage ('create-deploy-22Q1-container') {
            steps {
	        sh "docker run -itdp 80:80 --name 22Q1 httpd"
                sh "docker cp index.html 22Q1:/usr/local/apache2/htdocs/"
            }
        } 
    }
}
