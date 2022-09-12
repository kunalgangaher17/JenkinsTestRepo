def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsStepTestAppKunal", deployableName:"PRD",changesetNumber: "Chset-111")
                }
            }
        }
    }
}
