pipeline{
    agent any
    stages {
        stage('Lint HTML'){
            steps{
                sh 'echo "linting HTML"'
                sh 'tidy -q -e *.html'
            }
        }
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