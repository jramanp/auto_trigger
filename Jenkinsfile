pipeline {
    agent { label "${params.Jenkins_Node_Label}" }
    stages {
        stage('Batch_Script') {
            steps {
                git branch: 'master', credentialsId: 'Ram_Git_PWD', url: 'git clone https://git.ads.kp.org/bitbucket/scm/~janakiraman.x.pichandi_kp.org/auto_trigger.git'
                script {
                    def error
                    dir("C:\\Jenkins\\workspace\\SandBox\\TDaaS_Demo_Jobs\\Auto_Trigger\\data_file\\")
                    {
                            bat(script: "**.bat", returnStdout:true)
                    }
                }
            }
        }
    }
}