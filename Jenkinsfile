def changeset = ''
pipeline {
    agent any
    stages {                
         stage('GetSnapshot') {
            steps {
                script {
                    snDevOpsConfigGetSnapshots(applicationName: "Jenkins_test_app", changesetNumber: "Chset-17", outputFormat: "xml")
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
