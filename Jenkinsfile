pipeline {
    agent {label 'agent1'}  

    stages{

        
    //     stage('CI') {
    //         steps {
                    
    //             withCredentials([usernamePassword(credentialsId: 'Dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) { 
                
    //             sh """
                    
    //                 docker build -f dockerfile -t shassem/nodeapp:$BUILD_NUMBER .
    //                 docker login -u ${USERNAME} -p ${PASSWORD}
    //                 docker push shassem/nodeapp:$BUILD_NUMBER
                    
    //             """
                
    //             }    

    //         }
    //     }        
        
    //     stage('CD') {
    //         steps {
                    
    //                 sh "docker run -d -p 3000:3000 shassem/nodeapp:$BUILD_NUMBER"

    //         }
    //     }
    // }         

///////////////

    stage('Print Branch name') {
        steps {
                
             echo "${env.GIT_BRANCH}"

        }
    }    
    }
}   


   
   
        
        
        
        
        
