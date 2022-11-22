def changeset = ''
pipeline {
    agent any
    stages {                
         stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "Jenkins_test_app", deployableName: "Preprod", outputFormat: "xml")
                }
            }
        }
}
}
