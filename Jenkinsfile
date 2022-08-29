pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo('This is the building stage')
            }
        }
        stage('Test'){
            steps{
                sh '''
                sudo ssh -i /var/lib/jenkins/jenkins.pem -t -o StrictHostKeyChecking=no ubuntu@ec2-44-204-16-109.compute-1.amazonaws.com
                cd /var/www
                sudo rm -rf html
                sudo mkdir html
                cd html
                sudo git init
                sudo git remote add origin https://github.com/Fearreece/webhook.git
                sudo git pull origin main
                '''
            }
        }

    
    }
}