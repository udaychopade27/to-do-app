pipeline {
  agent any
      stages {
         stage ("code checkout"){
              steps {
                    echo "cloning code from github repo"
                     sh "git -v"
                  }                     
            }
         stage ("build"){
              steps { 
                    echo "building docker container"
                    sh "docker build -t to-do-app ."
     
                   }
            }
         stage ("deploy"){
              steps {
                    echo "run container"
                    sh "docker run -d -p 3000:3000 to-do-app"
                   }
            }
      }
}
