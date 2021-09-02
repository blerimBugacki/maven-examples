pipeline{
    agent any

<<<<<<< HEAD
    stages{
        stage("Build"){
            steps{
                sh "mvn -version"
                sh "mvn clean install"
            }
=======
    stages("Build"){
        steps{
            sh "mvn -version"
            sh "mvn clean install"
>>>>>>> 432a93121f8c71b21af36990a518f92f2e629d4f
        }
    }

    post{
        always{
            cleanWs()
        }
    }
<<<<<<< HEAD
}
=======
}
>>>>>>> 432a93121f8c71b21af36990a518f92f2e629d4f
