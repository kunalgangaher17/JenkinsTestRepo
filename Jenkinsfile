def changeset = ''
pipeline {
    agent any
    stages {
        stage('Upload') {
            steps {
                script {
                    changeset = snDevOpsConfigUpload(applicationName: "JenkinsStepTestAppKunal",target:"component",dataFormat:"json",configFile:"configComp.json",namePath:"Comp",autoCommit: false,autoValidate: true)
                    snDevOpsConfigUpload(applicationName: "JenkinsStepTestAppKunal",changesetNumber:"${changeset}",target:"deployable",dataFormat:"json",configFile:"configDepl.json",namePath:"Depl",deployableName:"PRD",autoCommit: true,autoValidate: true)
                }
            }
        }
        stage('Validate') {
            steps {
                script {
                    snDevOpsConfigValidate(applicationName: "JenkinsStepTestAppKunal",deployableName:"TST-1",snapshotName: "TST-1-v1.dpl")
                }
            }
        }
        stage('Publish') {
            steps {
            script {
                    snDevOpsConfigPublish(applicationName: "JenkinsStepTestAppKunal",deployableName:"PRD",snapshotName: "PRD-v2.dpl")
                }
            }
        }
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsStepTestAppKunal", changesetNumber: "Chset-111")
                }
            }
        }
        stage('ExportSnapshot'){
            steps{
                script {
                snDevOpsConfigExport(applicationName: "JenkinsStepTestAppKunal", deployableName: "PRD", exporterFormat:"json", exporterName:"keka-returnValueForUniqueKeyName",fileName:"exporterFile.json",snapshotName: "PRD-v1.dpl")
                }
            }
        }
    }
}
