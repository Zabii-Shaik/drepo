pipeline{
    agent any
    stages {
         stage( "code pull") {
            steps {
                git  'https://github.com/github6472/drepo.git'
                echo 'git pull successesful'
            }
        }
        stage ('code build') {
            steps {
                sh 'mvn install'
            }
        }
	stage ('code deploy') {
            steps {
                sh 'sshpass -p "nano6472" scp target/abcd.war 172.17.0.2:/home/dev_data/apache-tomcat-9.0.55/webapps'
            }
     }
 }
    

