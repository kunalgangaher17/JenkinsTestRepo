def changeset = ''
pipeline {
    agent any
    stages {        
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsStepTestAppKunal1", changesetNumber: "Chset-11")
                }
            }
        }
    }
}
