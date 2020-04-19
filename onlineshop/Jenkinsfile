node{

    stage('SCM Checkout')
    {
        git 'https://github.com/iamdevopstrainer/onlineshop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose down'
        sh 'docker-compose up -d'
    }
    
    stage('Push Docker Image to HUB')
    {
        sh 'sudo docker push iamdevopstrainer/deployapp_web'
    }
    
}
