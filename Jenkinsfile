pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
              checkout([$class: 'GitSCM', 
                branches: [[name: '*/main']],
                doGenerateSubmoduleConfigurations: false,
                extensions: [[$class: 'CleanCheckout']],
                submoduleCfg: [], 
                userRemoteConfigs: [[url: 'https://github.com/starx46/kubernatesprojects.git']]])
                sshCommand remote:remote, command: "ls -l"

          }
        }
    }
}
