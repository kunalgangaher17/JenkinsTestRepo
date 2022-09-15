def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsAppKunal", deployableName: "PRD", changesetNumber: "")
                }
            }
        }
    }
}
