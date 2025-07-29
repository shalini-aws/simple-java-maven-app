pipeline {
   agent {
  label 'Devserver'
}
    tools {
  maven 'my-maven'
       }

    stages {
        stage('Build')
        {
            steps {
                sh 'mvn clean package'
            }

        post {
  success {
        archiveArtifacts artifacts: '**/target/*.war'
           }
        }


        }
        
    }
}
