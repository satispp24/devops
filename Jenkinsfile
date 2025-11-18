pipeline {
    agent any
    environment {
         AWS_ACCESS_KEY_ID     = credentials('my-aws-creds')
         AWS_SECRET_ACCESS_KEY = credentials('my-aws-creds')
    }
    stages {
        stage('Submit Stack') {
            steps {
              sh "cat 01_s3cft.yml"
              sh "aws cloudformation create-stack --stack-name s3bucket --template-body file://01_s3cft.yml --region 'us-west-2'"
              }
             }
            }
            }
