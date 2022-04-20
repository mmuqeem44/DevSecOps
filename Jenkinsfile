pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
   
    
    stage('Check-Git-Secrets'){
        steps{
        sh 'rm trufflehog || true'
        sh 'docker pull gesellix/trufflehog'
        sh 'docker run -t gesellix/trufflehog --json https://github.com/mmuqeem44/DevSecOps.git > trufflehog'    
        sh 'cat trufflehog'    
        } 
    }
  }
}
