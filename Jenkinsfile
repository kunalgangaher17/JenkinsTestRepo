def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTestAppKunal2", deployableName: "PRD")
                }
            }
        }
    }
}
