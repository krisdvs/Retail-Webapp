pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git 'https://github.com/SudhirG85/Retail-Webapp.git'
                bat 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                bat 'set CATALINA_HOME=C:\MyApplications\apache-tomcat-8.5.9\necho %WORKSPACE%\ncd C:\MyApplications\apache-tomcat-8.5.9\bin\nCALL shutdown.bat\nCOPY %WORKSPACE%\target\retailone.war C:\MyApplications\apache-tomcat-8.5.9\webapps\\nCALL startup.bat'
            }
        }        
    }
}
