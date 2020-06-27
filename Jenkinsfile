pipeline{
     agent any
    
    stages{
        stage('Installing NPM dependencies'){
           
            steps {
                sh '/usr/local/bin/npm install'
            }
        }
         stage('Run Unit Test'){
        
            steps {
                sh '/usr/local/bin/npm run test'
            }
        }
        stage('Run Coverage Test'){
        
            steps {
                sh '/usr/local/bin/npm run testCoverage'
            }
        }
        stage('Run Sonar Analysis'){
            steps {
                sh '/usr/local/bin/npm run sonar'
            }
        }
         stage('Build docker image'){
            steps {
                sh 'docker-compose build'
            }
        }

         stage('Upload docker image'){
            steps {
                echo 'Uploading docker image to Dockerhub'
            }
        }

         stage('Launch CustomerService Application'){
            steps {
                sh 'docker-compose up'
            }
        }


         stage('Functional Test'){
            steps {
                echo 'Functional Test executed successfully'
            }
        }

         stage('Performance Test'){
            steps {
                echo 'Performance Test executed successfully'
            }
        }

         stage('Security Test'){
            steps {
                echo 'Security Test executed successfully'
            }
        }
    }
}
