pipeline{
    agent any

    stages{
        stage('Compile stage') {
    steps {
      sh '''
        mvn -version
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
