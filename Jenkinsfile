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
                sudo ssh -i /var/lib/jenkins/jenkins.pem -t  ubuntu@ec2-44-204-16-109.compute-1.amazonaws.com
                '''
            }
        }

    
    }
}