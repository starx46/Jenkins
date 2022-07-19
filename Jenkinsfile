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
                script{
                    def remote = [:]
                    remote.name = "friendly name"
                    remote.host = "172.31.88.95"                    
                    remote.user = 'root'
                    remote.password = 'root@123'
                    remote.allowAnyHosts = true
                    remote.identityFile = identity

           
                    sshCommand remote:remote, command: "ls -l"
                    sshCommand remote:remote, command: 'ls -l'
                    sshCommand remote:remote, command: 'pwd'
                }
          }
        }
    }
}
