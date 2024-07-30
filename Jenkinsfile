pipeline{
    agent any
    stages {

        stage('prod'){

      steps  {
            sh '''
            chmod +x prod.tf
            ./prod.tf
            '''
         }
      }  
        stage('dev'){
            steps {
                sh '''
                chmod +x dev.tf
                ./dev.tf
                '''
            }
        }
        stage('test'){
            steps {
                sh '''
                chmod +x test.tf
                ./test.tf
                '''
            }
        }  
    }
}
