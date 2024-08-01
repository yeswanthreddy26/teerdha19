
pipeline{
    agent any
    stages {
        stage('aws'){
            steps  {

        withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws-cred', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
    // some block
   }
 }           
}
        stage('dev'){

      steps  {
            sh '''
            dev.tf
            terraform init
            terraform plan
            terraform apply dev.tf -auto-approve
            '''
            }
        }
    }
}
