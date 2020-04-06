  
pipeline {
    agent any
    tools { 
        nodejs "node"
        sonarqube "sonarqube"
    }  
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
                                  sh 'npm install && npm run build --prod'
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
                                  //sh "npm run test"
                                  sh 'npm run test --progress false --watch false'
                    }
                    catch (e) {
                        //echo 'Something failed, I should scontact the Jenkins admin!'
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
                                  sh 'sonar-scanner -Dsonar.projectKey=node-test-app -Dsonar.sources=. -Dsonar.host.url=http://localhost:9000 -Dsonar.login=fec4425f79ad241358bcb890756c8e77245892d6'
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
