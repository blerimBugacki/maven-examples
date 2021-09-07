pipeline{
    agent any

    environment{
	MAVEN_HOME="/usr/local/Cellar/maven/3.8.2/libexec"
}

    stages{
        stage('Compile stage') {
    steps {
      sh '''
	PATH=$MAVEN_HOME:/usr/local/bin:$PATH
        cd java-project
        mvn package
        mvn clean compile
        '''
      }
    }
stage('Testing stage') {
      steps {
      sh '''
        PATH=$HOME/bin:/usr/local/bin:$PATH:$MAVEN_HOME:$BREW:$AZURE
        cd java-project
        mvn test
        '''
      }
    }
    stage('Final Jenkins Pipeline Stage') {
      steps {
      sh "echo 'Jenkins Pipeline Complete'"
      junit "java-project/target/surefire-reports/*.xml"
      }
    }


    }


    post{
        always{
            cleanWs()
        }
    }
}
