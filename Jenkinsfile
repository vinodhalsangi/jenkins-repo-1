pipeline {
    agent {
	label "slave-2"
    }

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'sudo mvn clean compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'sudo mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'sudo mvn install'
                }
            
        }
        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is dev branch"
                }
            
        }
    }
}
