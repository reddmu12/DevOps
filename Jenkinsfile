pipeline {
    agent any
    stages {
        stage('Check Jenkins Service Status') {
            steps {
                script {
                    def status = sh(script: 'systemctl status jenkins', returnStatus: true)
                    if (status != 0) {
                        error("Jenkins service is not running!")
                    }
                }
            }
        }
    }
}
