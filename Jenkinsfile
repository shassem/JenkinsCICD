pipeline {
    agent {label 'ec2agent'}  

    stages{

        
        stage('CI') {
            steps {
                    
                withCredentials([usernamePassword(credentialsId: 'Dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) { 
                
                sh """
                    
                    docker build -f dockerfile -t nodeapp:$BUILD_NUMBER .
                    docker login -u ${USERNAME} -p ${PASSWORD}
                    docker push nodeapp:$BUILD_NUMBER
                    
                """
                
                }    

            }
        }        
        
        stage('CD') {
            steps {
                    
                    sh "docker run -d -p 3000:3000 nodeapp:$BUILD_NUMBER"

            }
        }
    }         

//////////////

    // stage('Print Branch name') {
    //     steps {
                
    //          echo "${env.GIT_BRANCH}"

    //     }
    // }       


   
   
        
        
        
        
        
    }