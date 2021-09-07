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
    }


    post{
        always{
            cleanWs()
        }
    }
}
