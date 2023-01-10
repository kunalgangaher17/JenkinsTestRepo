def changeset = ''
pipeline {
    agent any
    stages {                
         stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "PassedWithExceptionTest", deployableName: "Production_1", outputFormat: "xml")
                }
            }
        }
}
}
