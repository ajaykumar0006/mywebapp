pipeline {
   agent any
   stages {
      stage('Checkout') {
steps {
git branch:'main', url:https://github.com/<user>/mywebapp.git'
      } 
}

stage('Build Docker Image') {
  steps {
    sh 'docker build -t mywebapp:latest .'
      }
}

stage('Run Container') {
  steps {
    sh 'docker stop mywebapp // true'
    sh 'docker run -d --name mywebapp -p 80:5000 mywebapp:latest' 
      }
    }
  }
      post {
            always { 
                  emailext to: 'ajaykr2047@gmail.com',
                  subject: "jenkins build status: $(currentBuild.currentResult"
                  body: "Build finished. Check jenkins for details."
} 
      }
}
