pipeline {
    agent {
    	label "slave-1"
    }

    stages {
	    stage ('maven install ') {
		
		    steps {
			    sh 'sudo yum install maven -y'
		    }
	    }
      stage ('Compile Stage') {

         steps {
           sh 'mvn clean compile'
         }
      }
      stage ('Testing Stage') {

         steps {
           sh 'mvn test'
         }
      }
      stage ('Install Stage') {
  
          steps {
             sh 'mvn install'
          }
       }
        
        stage ('Echo Branch') {

            steps {
                echo "This is master branch"
            } 
        }
    }
}
