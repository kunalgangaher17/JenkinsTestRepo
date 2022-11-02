def changeset = ''
pipeline {
    agent any
    stages {
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTestAppKunal1717", deployableName: "Production_1")
                }
            }
        }
    }
}
