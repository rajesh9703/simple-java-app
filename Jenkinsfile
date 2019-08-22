pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {                
                timeout(time: 3, unit: 'MINUTES') {
                retry(3) {
                    sh 'sh raj.sh'
                }
                }
            }
        }
    }
    port {
        always {
            sh 'echo "This will always run"'
        }
        success {
            sh 'echo "This will run only the build is success"'
        }
        failure {
            sh 'echo "This will only run when build failiure"'
        }
        unstable {
            sh 'echo "This will only run when build is unstable"'
        }
        changed {
            sh 'echo "This will run only if the state of the Pipeline has changed"'
            sh 'echo "For example, if the Pipeline was previously failing but is now successful"'
        }
}
                    
        
                
            
