def changeset = ''
pipeline {
    agent any
    stages {        
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsStepTestAppKunal", changesetNumber: "Chset-111")
                }
            }
        }
    }
}
