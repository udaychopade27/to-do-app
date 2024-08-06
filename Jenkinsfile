pipeline {
  agent any
      stages {
         stage ("clone code"){
              steps {
                    echo "cloning code from github repo"
                    git url: "https://github.com/udaychopade27/to-do-app.git", branch "main"
                     }
}
         stage ("build"){
              steps { 
                    echo "building docker container"
                    sh "docker build -t to-do-app to-do-app/"
     
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
