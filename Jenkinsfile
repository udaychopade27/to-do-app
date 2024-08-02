pipeline {
  agent any
      stages {
         stage ("clone code from github"){
              steps {
                    echo "cloning code from github repo"
                    git 'https://github.com/udaychopade27/to-do-app.git'
                     }
}
         stage ("build docker image"){
              steps { 
                    echo "building docker container"
                    sh "docker build -t to-do-app ."
     
                   }
}
         stage ("run container"){
              steps {
                    echo "run container"
                    sh "docker run -d -p 3000:3000 to-do-app"
                   }
}
}
}
