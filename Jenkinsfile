pipeline{
    agent any
    stages {

        stage('rds'){

      steps  {
            sh '''
            chmod +x rds.tf
            ./rds.tf
            '''}
        }
        stage('prod'){
            steps {
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
        stage('dev'){
            steps {
                sh '''
                chmod +x test.tf
                ./test.tf
                '''
    }
}
