def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTestAppKunal2", changesetNumber: "", deployableName: "PRD")
                }
            }
        }
    }
}
