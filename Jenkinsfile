node{

    stage('SCM Checkout')
    {
        git 'https://github.com/busykumar50/onlineshop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose down'
        sh 'sudo docker-compose up -d'
    }
    
    stage('Push Docker Image to dhub')
    {
        sh 'sudo docker push busykumar50/ecomdep'
    }
    
}
