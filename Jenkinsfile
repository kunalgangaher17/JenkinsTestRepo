def changeset = ''
pipeline {
    agent any
    stages {
        stage('Upload') {
            steps {
                script {
                    changeset = snDevOpsConfigUpload(applicationName: "JenkinsStepTestAppKunal",target:"component",dataFormat:"json",configFile:"",namePath:"Comp",autoCommit: false,autoValidate: true)
                    snDevOpsConfigUpload(applicationName: "JenkinsStepTestAppKunal",changesetNumber:"${changeset}",target:"deployable",dataFormat:"json",configFile:"",namePath:"Depl",deployableName:"PRD",autoCommit: true,autoValidate: true))
                }
            }
        }
    }
}
