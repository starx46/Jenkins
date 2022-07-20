pipeline {
    agent any
    stages {
        stage('SSH remote') {
            steps {
                 script {
                    def remote = [:]
                    remote.host = "172.31.88.95"                    
                    remote.user = 'root'
                    remote.password = 'root@123'
                    remote.allowAnyHosts = true
                    remote.identityFile = identity
                     sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
                 }
            }
        }
    }
}
