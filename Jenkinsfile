pipeline {

    agent any
    
    stages {
        
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
                
                echo "Cleaned Up Workspace For Project"
               
            }
        }

        stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '*/develop']], 
                    userRemoteConfigs: [[url: 'https://github.com/Sneha2597/ConsoleApp3.git']]
                ])
            }
        }

        stage(' Unit Testing') {
            steps {
              
                echo "Running the Unit Tests"
               
            }
        }

        stage('Code Analysis') {
            steps {
               
                echo "Running Code Analysis"
                
            }
        }

        stage('Build Deploy Code') {
            when {
                branch 'develop'
            }
            steps {
                
                echo "Building Artifact"
               

                
                echo "Deploying Code"
              
            }
        }

    }   
}
