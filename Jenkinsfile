def changeset = ''
pipeline {
    agent any
    stages {        
        stage('Validate') {
            steps {
            script {
                    snDevOpsConfigValidate(applicationName: "JenkinsTestAppKunal1717",deployableName:"Production_1",snapshotName: "Production_1-v1.dpl")
                }
            }
        }
    }
}
