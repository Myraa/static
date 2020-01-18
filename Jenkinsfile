pipeline{
    agent any
    stages {
        stage('build'){
            steps{
                sh 'echo "hello world"'
                sh '''
                    echo "multi line shell steps works too"
                    ls -alh
                    '''

            }
        }
    }
}