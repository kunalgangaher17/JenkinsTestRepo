def changeset = ''
pipeline {
    agent any
    stages {        
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsStepTestAppKunal2", changesetNumber: "Chset-20")
                }
            }
        }
    }
}
