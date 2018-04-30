pipeline {
        agent any 
            stages {
                stage('Build'){
                    steps{
                        sh "${MAVEN_HOME}/bin/mvn clean package"
                    }
                }
                stage('Test'){
                    steps{
                        sh "${MAVEN_HOME}/bin/mvn test"
                    }
                } 
                stage('Deploy_WebApp'){
                    steps{
                        sh 'scp -i /root/keys/id_rsa /WebApp.war devops
                    }
                }
            }
}
