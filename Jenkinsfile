pipeline {
    agent { 
docker { 
image 'python:3.7.2' 

} 

}
    stages {
        stage('build') {
            steps {
                sh 'sudo apt install-pip'
                sh 'sudo apt install-flask'
            }
        }
        stage('test') {
            steps {
                sh ' python test.py'
            }
            post {
                always {junit 'test-reports/*.xml'}
            }
        }
    }
}
