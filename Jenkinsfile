pipeline{
     agent any
    
    stages{
        stage('Installing NPM dependencies'){
           
            steps {
                sh 'npm install'
            }
        }
         stage('Run Unit Test'){
        
            steps {
                sh 'npm run test'
            }
        }
        stage('Run Coverage Test'){
        
            steps {
                sh 'npm run testCoverage'
            }
        }
        stage('Run Sonar Analysis'){
            steps {
                sh 'npm run sonar'
            }
        }
        /* stage('Build docker image'){
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
                sh 'docker-compose up -d'
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

         stage('Destroy Customer Service Application'){
            steps {
                sh 'docker-compose down'
            }
        }
        stage('Upload the docker image to Google container repository'){
            steps {
                sh 'gcloud builds submit --tag gcr.io/kuberenetes-01-basic/customer-service:1.0 .'
            }
        }
         stage('Launch Mongodb service'){
            steps {
                sh 'kubectl create -f mongodb.yaml'
            }
        }

        stage('Launch Customer service'){
            steps {
                sh 'kubectl create -f customerservice.yaml'
            }
            post {
                always{
                    echo 'Smoke Test run successfully'
                }
            }
        } */

    }
}
