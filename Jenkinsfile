pipeline {
        agent any 
        MAVEN_HOME=/root/maven/apache-maven-3.5.3/bin/mvn
            stages {
                stage('Build'){
                    steps{
                        sh "${MAVEN_HOME}/bin/mvn clean package"
                    }
                }
            }
}
