  
pipeline {
    agent any
    tools { nodejs "node"}  
    stages {
           stage('Checkout') {
            steps{
                script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  CHECKOUT STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                                  sh 'npm --version'
                    }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
            }
        }
        stage('Build') {
            steps {
                  script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  BUILD STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                                  sh 'npm install && npm install -g @angular/cli & ng build --prod'
            }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
            }
        }
        stage('Unit Test') {
            steps {
                                 script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  UNIT TEST STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                    }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
            }
        }
        stage ('Sonar Test') {
          steps {
                                           script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  SONAR TEST STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                    }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
          }
        }
        stage('Build stage') {
          steps {
                                                           script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  BUILD STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                    }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
          }
        }
        stage('Deploy') {
            steps {
                                                 script{
                    try {
						          echo '--------------------------------------------------------------------------------------------------------------------------'
						          echo '-                                                  DEPLOYMENT STAGE                                                        -'
						          echo '--------------------------------------------------------------------------------------------------------------------------'		
                    }
                    catch (e) {
                        echo 'Something failed, I should scontact the Jenkins admin!'
                        throw e
                    }    
                }
            }
        }
    }
}
