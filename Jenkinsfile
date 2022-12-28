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
                git branch: '22Q2', url: 'http://github.com/sayalip848/docker-assignment.git'
            }
        }       
stage ('create-deploy-22Q2-container') {
            steps {
	              sh "docker run -itdp 90:80 --name 22Q2 httpd"
                sh "docker cp index.html 22Q2:/usr/local/apache2/htdocs/"
            }
        } 
    }
}
