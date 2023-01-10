def changeset = 'Chset-27'
pipeline {
    agent any
    stages {
        stage('Upload') {
            steps {
                script {
                    changeset = snDevOpsConfigUpload(applicationName: "JenkinsTelemetryApp",target:"component",dataFormat:"json",configFile:"configComp.json",namePath:"Comp",autoCommit: false,autoValidate: true)
                    snDevOpsConfigUpload(applicationName: "JenkinsTelemetryApp",changesetNumber:"${changeset}",target:"deployable",dataFormat:"json",configFile:"configDepl.json",namePath:"Depl",deployableName:"Production_1",autoCommit: true,autoValidate: true)
                }
            }
        }        
        stage('Publish') {
            steps {
            script {
                    snDevOpsConfigPublish(applicationName: "JenkinsTelemetryApp",deployableName:"Production_1",snapshotName: "Production_1-v1.dpl")
                }
            }
        }
        stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "JenkinsTelemetryApp", changesetNumber: "Chset-27", outputFormat: "xml/json")
                }
            }
        }
        stage('ExportSnapshot'){
            steps{
                script {
                snDevOpsConfigExport(applicationName: "JenkinsTelemetryApp", deployableName: "Production_1", exporterFormat:"json", exporterName:"returnAllData-now",fileName:"exporterFile.json",snapshotName: "Production_1-v1.dpl")
                }
            }
        }
    }
}
