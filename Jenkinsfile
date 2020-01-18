pipeline{
    agent any
    stages {
        stage('Upload to AWS'){
            steps{
                withAWS(credentials: 'blueocean', region: 'us-east-1') {
                    sh 'echo "hello S3"'
                    s3Upload acl: 'Private', bucket: 'staticjenkinspboddubucket', file: 'index.html'
                }
            }
        }
    }
}