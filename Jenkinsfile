pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'gcc ./src/main.c -o testing'
            }
        }
        stage('Deploy') {
            steps {
                sh 'chmod +x testing'
                sh 'scp -i /home/jenkins/.ssh/id_rsa testing jesus@192.168.6.22:/tmp/testing.exe'
            }
        }
    }
}
