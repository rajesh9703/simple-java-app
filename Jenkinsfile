pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh './raj.sh'
                }
                
                timeout(time: 3, unit: 'MINUTES') {
                    sh './raj.sh'
                }
            }
        }
    }
}
                    
        
                
            
