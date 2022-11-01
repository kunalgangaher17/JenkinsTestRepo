def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsAppKunal", deployableName: "Production_1", changesetNumber: "Chset-6")
                }
            }
        }
    }
}
