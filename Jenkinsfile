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
    }
    post{
     always{        
         echo ">>>>>Displaying Test results"
          junit '**/*.xml'
          cleanWs()
     }
}
}
