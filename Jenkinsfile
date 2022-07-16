#! groovy
node {
    stage('code') {
        
        sh " git branch: 'main', url: 'https://github.com/cvsuneel/shoes-microservice-springboot.git' "
    }
    stage('Build') {
        sh 'docker build -t shoes .'
    }
    stage('Deploy') {
        sh 'docker run -d -p 1002:1002 --restart unless-stopped --name shoes shoes'
    }
}
