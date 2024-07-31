
pipeline{
    agent any
    stages {

        stage('dev'){

      steps  {
            sh '''
            terraform init
            terraform apply -var-file=dev.tfvars -auto-approve
            '''
            }
        }
        stage('prod'){
            steps {
                sh '''
                terraform init
                terraform apply -var-file=prod.tfvars -auto-approve
                '''
            }
        }
        stage('test'){
            steps {
                sh '''
                terraform init
                terraform apply -var-file=test.tfvars -auto-approve
                '''
            }
        }  
    }
}
