def changeset = ''
pipeline {
    agent any
    stages {        
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "NodesValueComparatorApp", deployableName: "Production_1")
                }
            }
        }
    }
}
