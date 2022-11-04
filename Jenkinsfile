def changeset = ''
pipeline {
    agent any
    stages {        
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTestApp", deployableName: "Production_1", outputFormat: "xml")
                }
            }
        }        
         stage('GetSnapshot1') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "NodesValueComparatorApp", deployableName: "Production_1", outputFormat: "xml")
                }
            }
        }
    }
}
