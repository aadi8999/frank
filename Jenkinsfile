pipeline {
    agent any

    stages {
        stage('Install AWS CLI') {
            steps {
                sh 'sudo apt update'
                sh 'sudo apt install awscli -y'
            }
        }
        stage('Deploy CloudFormation Stack') {
            steps {
                sh 'aws cloudformation create-stack --stack-name my-ec2-instance --template-body file://path/to/your-cloudformation.yml --parameters ParameterKey=KeyName,ParameterValue=your-key-pair'
            }
        }
    }
}
