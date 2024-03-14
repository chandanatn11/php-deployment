pipeline {
    agent any
    stages {
        stage('clean workspace')
	   {
           steps
           {
                    sh 'rm -r *'
                    sh 'rm -r /var/lib/jenkins/workspace/*'
                
           }
       }
       
       stage('Clone Project') 
       {
            steps 
            {
                     sh 'git clone https://github.com/chandanatn11/php-deployment.git -b main' 
            }
        }

        stage('deploy')
        {
              steps
            {
                sh ' mv /var/lib/jenkins/workspace/php-deployment/* ../../../../www/html/ '
	        }
	    }
     
   }
  
}
