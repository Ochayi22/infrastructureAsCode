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
               sh  'cd SampleWebApp && mvn clean install    
            
         }
      
       }         
                
          stage {'test'} {          
          steps {
              sh 'cd SampleWebApp && mvn test'
             
             
           }
        
         }
        stage {'Code Quality Scan' } {         
               
         steps      
                  
            }
        }
               
     }
    }
    
}
