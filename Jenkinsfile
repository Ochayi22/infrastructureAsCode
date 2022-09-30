pipeline {
    agent any
    
    stages   {
     stage('Git checkout') {
            steps {
               git 'https://github.com/tkibnyusuf/infrastructureAsCode.git'
        
         }
          
     }
       
        stage{'build with maven' }   {
            step   {
               sh  'cd    
            
        
        
        stage('provision server') {
           environment {
             AWS_ACCESS_KEY_ID = credentials('aws_access_key_id')
             AWS_SECRET_ACCESS_KEY = credentials('aws_secret_access_key')
           }
           steps {
              script {
                  sh "terraform init"
                  sh "terraform validate"
                  sh "terraform plan"
                  sh " terraform destroy --auto-approve"
            }
        }
               
     }
    }
    
}
