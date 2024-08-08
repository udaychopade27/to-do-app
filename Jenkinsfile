pipeline {
  agent any
      stages {
         stage ("code checkout"){
              steps {
                    echo "cloning code from github repo"
                     sh "git -v"
                     sh "docker --version"
                  }                     
            }
         stage("stop existing container"){
              steps{
                echo "stop running container"
                sh "docker-compose down"
              }
         }   
         stage ("build"){
              steps { 
                    echo "building docker container"
                    sh "docker-compose up -d"
     
                   }
            }
        // stage ("deploy"){
          //    steps {
            //        echo "run container"
              //      sh "docker run -d -p 3000:3000 to-do-app"
                //   }
           // }
      }
}
