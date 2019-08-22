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
           echo "This will always run"
        }
        success {
            echo "This will run only the build is success"
        }
        failure {
            echo "This will only run when build failiure"
        }
        unstable {
            echo "This will only run when build is unstable"
        }
        changed {
            echo "This will run only if the state of the Pipeline has changed"
            echo "For example, if the Pipeline was previously failing but is now successful"
        }
}
                    
        
                
            
