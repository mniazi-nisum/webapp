pipeline {
        agent any 
            stages {
                stage('Build'){
                    steps{
                        sh "/usr/local/maven/bin/mvn clean package"
                    }
                }
                stage('Test'){
                    steps{
                        sh "/usr/local/maven/bin/mvn test"
                    }
                } 
                stage('Deploy'){
                    steps{
                        when{
                            expression{
                                currentBuild.result==null || currentBuild.result == 'SUCCESS'
                            }
                        }
                    steps{
                        sh 'make publish'
                    }
                    }
                }
            }
}

