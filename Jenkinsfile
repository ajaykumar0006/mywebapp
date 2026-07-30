pipeline {
agent any

stages {

stage('Clone') {
steps {
git 'https://github.com/username/repo.git'
      } 
}

stage('Build Docker Image') {
steps {
sh 'docker build -t myapp .'
      }
}

stage('Run Docker') {
steps {
sh 'docker run -d -p 80:5000 myapp'
      }
    }
  }
}
