def changeset = ''
pipeline {
    agent any
    stages {
        stage('Publish') {
            steps {
            script {
                    snDevOpsConfigPublish(applicationName: "JenkinsTestAppKunal2",deployableName:"PRD",snapshotName: "PRD-v1.dpl")
                }
            }
        }
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTestAppKunal2", changesetNumber: "Chset-20", deployableName: "PRD")
                }
            }
        }
    }
}
